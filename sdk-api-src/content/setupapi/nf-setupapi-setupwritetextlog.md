---
UID: NF:setupapi.SetupWriteTextLog
title: SetupWriteTextLog function
author: windows-sdk-content
description: The SetupWriteTextLog function writes a log entry in a SetupAPI text log.
old-location: devinst\setupwritetextlog.htm
old-project: devinst
ms.assetid: 8a59c796-1386-495c-9790-8916d677ebd3
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: SetupWriteTextLog, SetupWriteTextLog function [Device and Driver Installation], devinst.setupwritetextlog, setupapi/SetupWriteTextLog, setupapilog-ref_42860a5c-0ea7-4185-81eb-76996286cafc.xml
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows Vista and later versions of Windows.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TSSD_ConnectionPoint, *PTSSD_ConnectionPoint
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.lib
 - Setupapi.dll
 - Ext-MS-Win-setupapi-logging-l1-1-0.dll
 - setupapi.dll
api_name:
 - SetupWriteTextLog
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: 
req.irql: 
req.product: ADAM
---

# SetupWriteTextLog function


## -description


The <b>SetupWriteTextLog</b> function writes a log entry in a <a href="devinst.setupapi_text_logs">SetupAPI text log</a>.


## -parameters




### -param LogToken [in]

A <a href="devinst.log_tokens">log token</a> that is either a system-defined log token or was returned by <a href="https://msdn.microsoft.com/library/windows/hardware/ff552211">SetupGetThreadLogToken</a>.


### -param Category [in]

A DWORD-typed value that indicates the event category for the log entry. The event categories that can be specified for a log entry are the same as those that can be enabled for a text log. For a list of event categories, see <a href="devinst.enabling_event_categories_for_a_text_log">Enabling Event Categories for a SetupAPI Text Log</a>. 


### -param Flags [in]

A DWORD-typed value that is a bitwise OR of flag values, which specify the following:

<ul>
<li>
The event level for the log entry. The event levels that can be specified for a log entry are the same as those that can be enabled for a text log. For a list of event level flags, see <a href="devinst.setting_the_event_level_for_a_text_log">Setting the Event Level for a SetupAPI Text Log</a>. 

</li>
<li>
Whether to include a time stamp in the log entry. The time stamp flag value is TXTLOG_TIMESTAMP.

</li>
<li>
The change, if any, to the indentation depth of the section and the current log entry. For information about how to use the indentation flags, see <a href="devinst.writing_indented_log_entries">Writing Indented Log Entries</a>.

</li>
</ul>

### -param MessageStr [in]

A pointer to a NULL-terminated constant string that contains a <b>printf</b>-compatible format string, which specifies the formatted message to include in the log entry. The comma-separated parameter list that follows <i>MessageStr</i> must match the format specifiers in the format string. 


### -param param

TBD




####### - ...

A comma-separated parameter list that matches the format specifiers in the format string that is supplied by <i>MessageStr</i>. 


## -returns



None




## -remarks



If the value of <i>LogToken</i> was returned by a call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff552211">SetupGetThreadLogToken</a> and the corresponding text log section can be found, <b>SetupWriteTextLog</b> writes the log entry in that text log section. If <b>SetupWriteTextLog</b> cannot locate the section, <b>SetupWriteTextLog</b> writes the log entry in the corresponding text log, but does not include the log entry in a section.

If the value of <i>LogToken</i> is one of the system-defined log tokens listed in the following table, <b>SetupWriteTextLog</b> performs the write operation that is indicated for that log token.

<table>
<tr>
<th>System-defined log token </th>
<th>Write operation</th>
</tr>
<tr>
<td>
LOGTOKEN_NOLOG

</td>
<td>
The log entry is not written to any text log.

</td>
</tr>
<tr>
<td>
LOG_TOKEN_UNSPECIFIED

</td>
<td>
The log entry is written to the application installation text log. The log entry is not included in a <a href="devinst.format_of_a_text_log_section">text log section</a>. 

</td>
</tr>
<tr>
<td>
LOGTOKEN_SETUPAPI_APPLOG

</td>
<td>
The log entry is written to the application installation text log. The log entry is not included in a text log section.

</td>
</tr>
<tr>
<td>
LOGTOKEN_SETUPAPI_DEVLOG

</td>
<td>
The log entry is written to the device installation text log. The log entry is not included in a text log section.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  Setting the value of <i>LogToken</i> to one of the system-defined log tokens does not change the value of the current log token for the thread.</div>
<div> </div>
In addition, <b>SetupWriteTextLog</b> does not write a log entry when any of the following are true:

<ul>
<li>
The <a href="devinst.setting_the_event_level_for_a_text_log">event level set for the text log</a> is less than the event level that is specified for the log entry. 

</li>
<li>
The event category for the log entry is not enabled for the text log. For more information about event categories, see <a href="devinst.enabling_event_categories_for_a_text_log">Enabling Event Categories for a Text Log</a>.

</li>
</ul>
The maximum length, in characters, of a log entry is 336.

To write information about a SetupAPI-specific error or a Win32 error in a text log, an application can use <a href="https://msdn.microsoft.com/library/windows/hardware/ff552232">SetupWriteTextLogError</a>.

For general information about writing log entries in the SetupAPI text logs, see <a href="devinst.setupapi_logging__windows_vista_and_later_">SetupAPI Logging (Windows Vista and Later)</a>. 

For more information about the operation of <b>SetupWriteTextLog</b>, see <a href="devinst.calling_setupwritetextlog">Calling SetupWriteTextLog</a>. 

For more information about log tokens, see <a href="devinst.log_tokens">Log Tokens</a>.

For more information about using log tokens, see <a href="devinst.setting_and_getting_a_log_token_for_a_thread">Setting and Getting a Log Token for a Thread</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552211">SetupGetThreadLogToken</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552232">SetupWriteTextLogError</a>
 

 

