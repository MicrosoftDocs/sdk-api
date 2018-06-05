---
UID: NF:setupapi.SetupWriteTextLogError
title: SetupWriteTextLogError function
author: windows-sdk-content
description: The SetupWriteTextLogError function writes information about a SetupAPI-specific error or a Win32 system error to a SetupAPI text log.
old-location: devinst\setupwritetextlogerror.htm
old-project: devinst
ms.assetid: 9b52d5a7-4a7f-49eb-86c4-cc0434b54232
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: SetupWriteTextLogError, SetupWriteTextLogError function [Device and Driver Installation], devinst.setupwritetextlogerror, setupapi/SetupWriteTextLogError, setupapilog-ref_886f507a-408e-4745-b9d2-ea0cf1bf7250.xml
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
-	APIRef
-	kbSyntax
api_type:
-	LibDef
api_location:
-	Setupapi.lib
-	Setupapi.dll
api_name:
-	SetupWriteTextLogError
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# SetupWriteTextLogError function


## -description


The <b>SetupWriteTextLogError</b> function writes information about a SetupAPI-specific error or a Win32 system error to a <a href="devinst.setupapi_text_logs">SetupAPI text log</a>.


## -parameters




### -param LogToken [in]

A <a href="devinst.log_tokens">log token</a> that is either a system-defined log token or was returned by <a href="https://msdn.microsoft.com/library/windows/hardware/ff552211">SetupGetThreadLogToken</a>.


### -param Category [in]

A value of type DWORD that indicates the event category for the log entry. The event categories that can be specified for a log entry are the same as those that can be enabled for a text log. For a list of event categories, see <a href="devinst.enabling_event_categories_for_a_text_log">Enabling Event Categories for a SetupAPI Text Log</a>. 


### -param LogFlags [in]

A value of type DWORD that is a bitwise OR of flag values, which specify the following:

<ul>
<li>
The event level for the log entry. The event levels that can be specified for a log entry are the same as those that can be enabled for a text log. For a list of event level flags, see <a href="devinst.setting_the_event_level_for_a_text_log">Setting the Event Level for a Text Log</a>. 

</li>
<li>
Whether to include a time stamp in the log entry. The time stamp flag value is TXTLOG_TIMESTAMP.

</li>
<li>
The change, if any, to the indentation depth of the section and the current log entry. For information about how to use the indentation flags, see <a href="devinst.writing_indented_log_entries">Writing Indented Log Entries</a>.

</li>
</ul>

### -param Error [in]

A SetupAPI-specific error code or a Win32 error code. The SetupAPI-specific error codes are listed in <i>Setupapi.h</i>. The Win32 error codes are listed in <i>Winerror.h</i>.


### -param MessageStr [in]

A pointer to a NULL-terminated constant string that contains a <b>printf</b>-compatible format string, which specifies the formatted message to include in the log entry. 


### -param param

TBD




####### - ...

A comma-separated parameter list that matches the format specifiers in the format string that is supplied by <i>MessageStr</i>. 


## -returns



None




## -remarks



If an installation application has a SetupAPI-specific error code or a Win32 error code that is associated with an installation error, the application can call <b>SetupWriteTextLogError</b> instead of <a href="https://msdn.microsoft.com/library/windows/hardware/ff552218">SetupWriteTextLog</a> to write two entries into a text log. The first entry will be the same as that written by <b>SetupWriteTextLog</b> and the second entry will log the error code and a user-friendly description of the error.

The log token, event category, and flags that a caller supplies affect the operation of <b>SetupWriteTextLogError</b> is the same manner as that described for <b>SetupWriteTextLog</b>.

<b>SetupWriteTextLogError</b> writes the first log entry in the following format: 

<i>
     entry-prefix</i>  <i>time_stamp category</i>
      <i>indentation</i>  <i>formatted-message</i>

<b>SetupWriteTextLogError</b> writes the second log entry in the following format:

<i>entry-prefix</i>  <i>time_stamp</i>  <i>category</i> 
     <i>indentation</i>  
     <b>Error:</b> <i>error-numbererror-description</i>

Where:

<ul>
<li>
The <i>entry-prefix</i>, <i>time-stamp</i>, <i>category</i>, <i>indentation</i>, and <i>formatted-message</i> fields are the same as those described in <a href="devinst.format_of_a_text_log_section_body">Format of a Text Log Section Body</a>.

</li>
<li>
The <i>error-number</i> field contains the error number.

</li>
<li>
The <i>error-description</i> field contains a user-friendly description of the error.

</li>
</ul>
For general information about writing log entries in the SetupAPI text logs, see <a href="devinst.setupapi_logging__windows_vista_and_later_">SetupAPI Logging (Windows Vista)</a>. 

For more information about the operation of <b>SetupWriteTextLogError</b>, see <a href="devinst.calling_setupwritetextlogerror">Calling SetupWriteTextLogError</a>. 

For more information about log tokens, see <a href="devinst.log_tokens">Log Tokens</a>.

For more information about using log tokens, see <a href="devinst.setting_and_getting_a_log_token_for_a_thread">Setting and Getting a Log Token for a Thread</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552211">SetupGetThreadLogToken</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552218">SetupWriteTextLog</a>
 

 

