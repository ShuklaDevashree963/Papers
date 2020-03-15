# Papers

<hr>
:toc: macro
:toc-title:
:toclevels: 99
# Title

toc::[]

## A

### A2

## B

### B2

== First ==

== Second ==

<table>
<thead>
<tr>
<th>Parameter</th>
<th>Description</th>
<th>Mandatory</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>p_file</code></td>
<td>Input spreadsheet file (.xlsx, .xlsm, .xlsb, .xls, .xml or .ods format) as a BLOB, or flat file, as a CLOB. <br>Helper functions <a href="#getfile-function">getFile()</a> and <a href="#gettextfile-function">getTextFile()</a> are available to directly reference the file from a directory.</td>
<td>Yes</td>
</tr>
<tr>
<td><code>p_sheet</code></td>
<td><em><strong>Spreadsheet only</strong></em> <br>Sheet name. <br>This parameter is interpreted as a regular expression pattern, if the feature has been enabled via <a href="#usesheetpattern-procedure">useSheetPattern</a> procedure (see note below).</td>
<td>Yes</td>
</tr>
<tr>
<td><code>p_sheets</code></td>
<td><em><strong>Spreadsheet only</strong></em> <br>Sheet list, of <code>ExcelTableSheetList</code> data type. <br>Provides a list of sheet names, e.g. <code>ExcelTableSheetList('Sheet1','Sheet2','Sheet3')</code></td>
<td>Yes</td>
</tr>
<tr>
<td><code>p_cols</code></td>
<td>Column list (see <a href="#columns-syntax-specification">specs</a> below)</td>
<td>Yes</td>
</tr>
<tr>
<td><code>p_range</code></td>
<td><em><strong>Spreadsheet only</strong></em> <br>Excel-like range expression that defines the table boundaries in the worksheet (see <a href="#range-syntax-specification">specs</a> below)</td>
<td>No</td>
</tr>
<tr>
<td><code>p_method</code></td>
<td><em><strong>Spreadsheet only</strong></em> <br>Read method. <br><code>DOM_READ</code> : 0 (default value), or <code>STREAM_READ</code> : 1. <br>This parameter is ignored if the file is not a .xlsx or .xlsm file.</td>
<td>No</td>
</tr>
<tr>
<td><code>p_password</code></td>
<td><em><strong>Spreadsheet only</strong></em> <br>Password used to encrypt the spreadsheet document.</td>
<td>No</td>
</tr>
<tr>
<td><code>p_skip</code></td>
<td><em><strong>Flat file only</strong></em> <br>Number of line(s) to skip from the beginning of the file. <br>For technical reasons, this parameter is mandatory, so set it explicitly to 0 by default if no line has to be skipped.</td>
<td>Yes</td>
</tr>
<tr>
<td><code>p_line_term</code></td>
<td><em><strong>Flat file only</strong></em> <br>Line terminator. At most two characters are allowed for this parameter, typically &lt;LF&gt; or &lt;CR&gt;&lt;LF&gt;.</td>
<td>Yes</td>
</tr>
<tr>
<td><code>p_field_sep</code></td>
<td><em><strong>Flat file only</strong></em> <br>Field separator. Must be exactly one character. <br>Mandatory for delimited flat files</td>
<td>No</td>
</tr>
<tr>
<td><code>p_text_qual</code></td>
<td><em><strong>Flat file only</strong></em> <br>Text qualifier. Must be exactly one character, typically " (QUOTATION MARK) or ' (APOSTROPHE). <br>Line terminators and field separators occurring in fields enclosed by this character won't be interpreted.</td>
<td>No</td>
</tr>
</tbody>
</table>

<ul>
<li>Added new streaming read method</li>
<li>Added setFetchSize() procedure</li>
</ul>
