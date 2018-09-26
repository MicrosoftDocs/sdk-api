---
UID: NF:setupapi.SetupWriteTextLogInfLine
title: SetupWriteTextLogInfLine function
author: windows-sdk-content
description: The SetupWriteTextLogInfLine function writes a log entry in a SetupAPI text log that contains the text of a specified INF file line.
old-location: devinst\setupwritetextloginfline.htm
tech.root: devinst
ms.assetid: 79386854-8b6b-4836-b8f3-d70657f6162c
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: SetupWriteTextLogInfLine, SetupWriteTextLogInfLine function [Device and Driver Installation], devinst.setupwritetextloginfline, setupapi/SetupWriteTextLogInfLine, setupapilog-ref_f6f9d000-dcfd-4dda-8a2c-bac81274a836.xml
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
api_name:
 - SetupWriteTextLogInfLine
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetupWriteTextLogInfLine function


## -description


The <b>SetupWriteTextLogInfLine</b> function writes a log entry in a <a href="devinst.setupapi_text_logs">SetupAPI text log</a> that contains the text of a specified INF file line.


## -parameters




### -param LogToken [in]

A <a href="devinst.log_tokens">log token</a> that is either a system-defined log token or was returned by <a href="https://msdn.microsoft.com/a4d870d0-2a1a-4319-9e52-e5bf469c4cdf">SetupGetThreadLogToken</a>.


### -param Flags [in]

A value of type DWORD that is a bitwise OR of flag values, which specify the following:

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

### -param InfHandle [in]

A handle to the INF file that includes the line of text to be written to the text log. A handle to an INF file is obtained by calling <b>SetupOpenInfFile</b>, which is documented in the Platform SDK.


### -param Context [in]

A pointer to an INF file context that specifies the  line of text to be written to the text log. An INF file context for a line is obtained by calling the <b>SetupFind</b><i>Xxx</i><b>Line</b> functions. For information about INF files and an INF file context, see the information that is provided in the Platform SDK about using INF files, obtaining an INF file context, and the INFCONTEXT structure. 


## -returns



None




## -remarks



<b>SetupWriteTextLogInfLine</b> writes a log entry in the following format:

<i>entry-prefix</i>  <i>time-stamp</i> <b>inf:</b><i>indentation</i> <i>inf-line-text</i> <b>(</b><i>inf-file-name</i> <b>line</b> <i>line-number</i><b>)</b>

Where:

<ul>
<li>
The <i>entry-prefix</i> and <i>time-stamp</i> fields are the same as those described in <a href="devinst.format_of_a_text_log_section_body">Format of a Text Log Section Body</a>.

</li>
<li>
The <i>inf-line-text</i> field contains the text of the specified INF file line. 

</li>
<li>
The <i>inf-file-name</i> field contains the name of the INF file that contains the specified INF file line.

</li>
<li>
The <i>line-number</i> field contains the line number of the specified line in the INF file.

</li>
</ul>
The log token and flags that a caller supplies affect the operation of <b>SetupWriteTextLogInfLine</b> in the same manner as that described for <a href="https://msdn.microsoft.com/8a59c796-1386-495c-9790-8916d677ebd3">SetupWriteTextLog</a> and <a href="https://msdn.microsoft.com/9b52d5a7-4a7f-49eb-86c4-cc0434b54232">SetupWriteTextLogError</a>. In addition, <b>SetupWriteTextLogInfLine</b> uses the <a href="devinst.enabling_event_categories_for_a_text_log">event category</a> TXTLOG_INF. 

For general information about writing log entries in the SetupAPI text logs, see <a href="devinst.setupapi_logging__windows_vista_and_later_">SetupAPI Logging (Windows Vista)</a>. 

For more information about the operation of <b>SetupWriteTextLogInfLine</b>, see <a href="devinst.calling_setupwritetextloginfline">Calling SetupWriteTextLogInfLine</a>. 

For more information about the various types of log tokens, see <a href="devinst.log_tokens">Log Tokens</a>.

For more information about using log tokens, see <a href="devinst.setting_and_getting_a_log_token_for_a_thread">Setting and Getting a Log Token for a Thread</a>.




## -see-also




<a href="https://msdn.microsoft.com/a4d870d0-2a1a-4319-9e52-e5bf469c4cdf">SetupGetThreadLogToken</a>



<a href="https://msdn.microsoft.com/8a59c796-1386-495c-9790-8916d677ebd3">SetupWriteTextLog</a>



<a href="https://msdn.microsoft.com/9b52d5a7-4a7f-49eb-86c4-cc0434b54232">SetupWriteTextLogError</a>
 

 

