---
UID: NF:pdh.PdhOpenLogA
title: PdhOpenLogA function (pdh.h)
description: Opens the specified log file for reading or writing. (ANSI)
helpviewer_keywords: ["PDH_LOG_CREATE_ALWAYS", "PDH_LOG_CREATE_NEW", "PDH_LOG_OPEN_ALWAYS", "PDH_LOG_OPEN_EXISTING", "PDH_LOG_OPT_CIRCULAR", "PDH_LOG_READ_ACCESS", "PDH_LOG_TYPE_BINARY", "PDH_LOG_TYPE_CSV", "PDH_LOG_TYPE_SQL", "PDH_LOG_TYPE_TSV", "PDH_LOG_TYPE_UNDEFINED", "PDH_LOG_UPDATE_ACCESS", "PDH_LOG_USER_STRING", "PDH_LOG_WRITE_ACCESS", "PdhOpenLogA", "pdh/PdhOpenLogA"]
old-location: perf\pdhopenlog.htm
tech.root: perf
ms.assetid: a8457959-af3a-497f-91ca-0876cbb552cc
ms.date: 12/05/2018
ms.keywords: PDH_LOG_CREATE_ALWAYS, PDH_LOG_CREATE_NEW, PDH_LOG_OPEN_ALWAYS, PDH_LOG_OPEN_EXISTING, PDH_LOG_OPT_CIRCULAR, PDH_LOG_READ_ACCESS, PDH_LOG_TYPE_BINARY, PDH_LOG_TYPE_CSV, PDH_LOG_TYPE_SQL, PDH_LOG_TYPE_TSV, PDH_LOG_TYPE_UNDEFINED, PDH_LOG_UPDATE_ACCESS, PDH_LOG_USER_STRING, PDH_LOG_WRITE_ACCESS, PdhOpenLog, PdhOpenLog function [Perf], PdhOpenLogA, PdhOpenLogW, _win32_pdhopenlog, base.pdhopenlog, pdh/PdhOpenLog, pdh/PdhOpenLogA, pdh/PdhOpenLogW, perf.pdhopenlog
req.header: pdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PdhOpenLogW (Unicode) and PdhOpenLogA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Pdh.lib
req.dll: Pdh.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PdhOpenLogA
 - pdh/PdhOpenLogA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Pdh.dll
api_name:
 - PdhOpenLog
 - PdhOpenLogA
 - PdhOpenLogW
---

# PdhOpenLogA function


## -description

Opens the specified log file for reading or writing.

## -parameters

### -param szLogFileName [in]

<b>Null</b>-terminated string that specifies the name of the log file to open. The name can contain an absolute or relative path. 




If the <i>lpdwLogType</i> parameter is <b>PDH_LOG_TYPE_SQL</b>, specify the name of the log file in the form, <b>SQL:</b><i>DataSourceName</i><b>!</b><i>LogFileName</i>.

### -param dwAccessFlags [in]

Type of access to use to open the log file. Specify one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PDH_LOG_READ_ACCESS"></a><a id="pdh_log_read_access"></a><dl>
<dt><b>PDH_LOG_READ_ACCESS</b></dt>
</dl>
</td>
<td width="60%">
Open the log file for reading.

</td>
</tr>
<tr>
<td width="40%"><a id="PDH_LOG_WRITE_ACCESS"></a><a id="pdh_log_write_access"></a><dl>
<dt><b>PDH_LOG_WRITE_ACCESS</b></dt>
</dl>
</td>
<td width="60%">
Open a new log file for writing. 

</td>
</tr>
<tr>
<td width="40%"><a id="PDH_LOG_UPDATE_ACCESS"></a><a id="pdh_log_update_access"></a><dl>
<dt><b>PDH_LOG_UPDATE_ACCESS</b></dt>
</dl>
</td>
<td width="60%">
Open an existing log file for writing.

</td>
</tr>
</table>
 

You can use the bitwise inclusive  <b>OR</b> operator (|) to combine the access type with one or more of the following creation flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PDH_LOG_CREATE_NEW"></a><a id="pdh_log_create_new"></a><dl>
<dt><b>PDH_LOG_CREATE_NEW</b></dt>
</dl>
</td>
<td width="60%">
Creates a new log file with the specified name.

</td>
</tr>
<tr>
<td width="40%"><a id="PDH_LOG_CREATE_ALWAYS"></a><a id="pdh_log_create_always"></a><dl>
<dt><b>PDH_LOG_CREATE_ALWAYS</b></dt>
</dl>
</td>
<td width="60%">
Creates a new log file with the specified name. If the log file already exists, the function removes the existing log file before creating the new file.

</td>
</tr>
<tr>
<td width="40%"><a id="PDH_LOG_OPEN_EXISTING"></a><a id="pdh_log_open_existing"></a><dl>
<dt><b>PDH_LOG_OPEN_EXISTING</b></dt>
</dl>
</td>
<td width="60%">
Opens an existing log file with the specified name. If a log file with the specified name does not exist, this is equal to PDH_LOG_CREATE_NEW.

</td>
</tr>
<tr>
<td width="40%"><a id="PDH_LOG_OPEN_ALWAYS"></a><a id="pdh_log_open_always"></a><dl>
<dt><b>PDH_LOG_OPEN_ALWAYS</b></dt>
</dl>
</td>
<td width="60%">
Opens an existing log file with the specified name or creates a new log file with the specified name.

</td>
</tr>
<tr>
<td width="40%"><a id="PDH_LOG_OPT_CIRCULAR"></a><a id="pdh_log_opt_circular"></a><dl>
<dt><b>PDH_LOG_OPT_CIRCULAR</b></dt>
</dl>
</td>
<td width="60%">
Creates a circular log file with the specified name. When the file reaches the value of the <i>dwMaxSize</i> parameter, data wraps to the beginning of the log file. You can specify this flag only if the <i>lpdwLogType</i> parameter is <b>PDH_LOG_TYPE_BINARY</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="PDH_LOG_USER_STRING"></a><a id="pdh_log_user_string"></a><dl>
<dt><b>PDH_LOG_USER_STRING</b></dt>
</dl>
</td>
<td width="60%">
Used with <b>PDH_LOG_TYPE_TSV</b> to write the user caption or log file description indicated by the <i>szUserString</i> parameter of <a href="/windows/desktop/api/pdh/nf-pdh-pdhupdateloga">PdhUpdateLog</a> or <b>PdhOpenLog</b>. The user caption or log file description is written  as the  last column in the first line of the text log.

</td>
</tr>
</table>

### -param lpdwLogType [in]

Type of log file to open. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PDH_LOG_TYPE_UNDEFINED"></a><a id="pdh_log_type_undefined"></a><dl>
<dt><b>PDH_LOG_TYPE_UNDEFINED</b></dt>
</dl>
</td>
<td width="60%">
Undefined log file format. If specified, PDH determines the log file type. You cannot specify this value if the <i>dwAccessFlags</i> parameter is <b>PDH_LOG_WRITE_ACCESS</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="PDH_LOG_TYPE_CSV"></a><a id="pdh_log_type_csv"></a><dl>
<dt><b>PDH_LOG_TYPE_CSV</b></dt>
</dl>
</td>
<td width="60%">
Text file containing column headers in the first line, and individual data records in each subsequent line. The fields of each data  record are comma-delimited.

The first line also contains information about the format of the file, the PDH version used to create the log file, and the names and paths of each of the counters.

</td>
</tr>
<tr>
<td width="40%"><a id="PDH_LOG_TYPE_SQL"></a><a id="pdh_log_type_sql"></a><dl>
<dt><b>PDH_LOG_TYPE_SQL</b></dt>
</dl>
</td>
<td width="60%">
The data source of the log file is an SQL database.

</td>
</tr>
<tr>
<td width="40%"><a id="PDH_LOG_TYPE_TSV"></a><a id="pdh_log_type_tsv"></a><dl>
<dt><b>PDH_LOG_TYPE_TSV</b></dt>
</dl>
</td>
<td width="60%">
Text file containing column headers in the first line, and individual data records in each subsequent line. The fields of each data  record are tab-delimited.

The first line also contains information about the format of the file, the PDH version used to create the log file, and the names and paths of each of the counters.

</td>
</tr>
<tr>
<td width="40%"><a id="PDH_LOG_TYPE_BINARY"></a><a id="pdh_log_type_binary"></a><dl>
<dt><b>PDH_LOG_TYPE_BINARY</b></dt>
</dl>
</td>
<td width="60%">
Binary log file format.

</td>
</tr>
</table>

### -param hQuery [in]

Specify a query handle if you are writing query data to a log file. The 
<a href="/windows/desktop/api/pdh/nf-pdh-pdhopenquerya">PdhOpenQuery</a> function returns this handle. 




This parameter is ignored and should be <b>NULL</b> if you are reading from the log file.

### -param dwMaxSize [in]

Maximum size of the log file, in bytes. Specify the maximum size if you want to limit the file size or if <i>dwAccessFlags</i> specifies <b>PDH_LOG_OPT_CIRCULAR</b>; otherwise, set to 0.

For circular log files, you must specify a value large enough to hold at least one sample.   Sample size depends on data being collected. However, specifying a value of at least one megabyte will cover most samples.

### -param szUserCaption [in]

<b>Null</b>-terminated string that specifies the user-defined caption of the log file. A log file caption generally describes the contents of the log file. When an existing log file is opened, the value of this parameter is ignored.

### -param phLog [out]

Handle to the opened log file.

## -returns

If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="/windows/desktop/Debug/system-error-codes">system error code</a> or a 
<a href="/windows/desktop/PerfCtrs/pdh-error-codes">PDH error code</a>.

## -remarks

To use this function to write performance data to a log file, you must open a query using 
<a href="/windows/desktop/api/pdh/nf-pdh-pdhopenquerya">PdhOpenQuery</a> and add the desired counters to it, before calling this function.

Newer operating systems can read log files that were generated on older operating systems; however, log files that were created on Windows Vista and later operating systems cannot be read on earlier operating systems.

The following rules apply to log files

- READ_ACCESS requires OPEN_EXISTING.

- UPDATE_ACCESS cannot be used with file-based logs. It can only be used with database logs.

- WRITE_ACCESS requires one of CREATE_NEW, CREATE_ALWAYS, OPEN_EXISTING, OPEN_ALWAYS.

#### Examples

For an example, see 
<a href="/windows/desktop/PerfCtrs/writing-performance-data-to-a-log-file">Writing Performance Data to a Log File</a>.

<div class="code"></div>




> [!NOTE]
> The pdh.h header defines PdhOpenLog as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/pdh/nf-pdh-pdhgetlogfilesize">PdhGetLogFileSize</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhopenquerya">PdhOpenQuery</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhupdateloga">PdhUpdateLog</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhupdatelogfilecatalog">PdhUpdateLogFileCatalog</a>
