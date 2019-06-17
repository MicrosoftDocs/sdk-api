---
UID: NF:setupapi.SetupWriteTextLogError
title: SetupWriteTextLogError function (setupapi.h)
author: windows-sdk-content
description: The SetupWriteTextLogError function writes information about a SetupAPI-specific error or a Win32 system error to a SetupAPI text log.
old-location: devinst\setupwritetextlogerror.htm
tech.root: devinst
ms.assetid: 9b52d5a7-4a7f-49eb-86c4-cc0434b54232
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SetupWriteTextLogError, SetupWriteTextLogError function [Device and Driver Installation], devinst.setupwritetextlogerror, setupapi/SetupWriteTextLogError, setupapilog-ref_886f507a-408e-4745-b9d2-ea0cf1bf7250.xml
ms.topic: function
f1_keywords: ["setupapi/SetupWriteTextLogError"]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Setupapi.lib
 - Setupapi.dll
api_name:
 - SetupWriteTextLogError
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetupWriteTextLogError function


## -description


The <b>SetupWriteTextLogError</b> function writes information about a SetupAPI-specific error or a Win32 system error to a <a href="https://docs.microsoft.com/windows-hardware/drivers/install/setupapi-text-logs">SetupAPI text log</a>.


## -parameters




### -param LogToken [in]

A <a href="https://docs.microsoft.com/windows-hardware/drivers/install/log-tokens">log token</a> that is either a system-defined log token or was returned by <a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupgetthreadlogtoken">SetupGetThreadLogToken</a>.


### -param Category [in]

A value of type DWORD that indicates the event category for the log entry. The event categories that can be specified for a log entry are the same as those that can be enabled for a text log. For a list of event categories, see <a href="https://docs.microsoft.com/windows-hardware/drivers/install/enabling-event-categories-for-a-text-log">Enabling Event Categories for a SetupAPI Text Log</a>. 


### -param LogFlags [in]

A value of type DWORD that is a bitwise OR of flag values, which specify the following:

<ul>
<li>
The event level for the log entry. The event levels that can be specified for a log entry are the same as those that can be enabled for a text log. For a list of event level flags, see <a href="https://docs.microsoft.com/windows-hardware/drivers/install/setting-the-event-level-for-a-text-log">Setting the Event Level for a Text Log</a>. 

</li>
<li>
Whether to include a time stamp in the log entry. The time stamp flag value is TXTLOG_TIMESTAMP.

</li>
<li>
The change, if any, to the indentation depth of the section and the current log entry. For information about how to use the indentation flags, see <a href="https://docs.microsoft.com/windows-hardware/drivers/install/writing-indented-log-entries">Writing Indented Log Entries</a>.

</li>
</ul>

### -param Error [in]

A SetupAPI-specific error code or a Win32 error code. The SetupAPI-specific error codes are listed in <i>Setupapi.h</i>. The Win32 error codes are listed in <i>Winerror.h</i>.


### -param MessageStr [in]

A pointer to a NULL-terminated constant string that contains a <b>printf</b>-compatible format string, which specifies the formatted message to include in the log entry. 


### -param arg6

A comma-separated parameter list that matches the format specifiers in the format string that is supplied by <i>MessageStr</i>. 


## -returns



None




## -remarks



If an installation application has a SetupAPI-specific error code or a Win32 error code that is associated with an installation error, the application can call <b>SetupWriteTextLogError</b> instead of <a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupwritetextlog">SetupWriteTextLog</a> to write two entries into a text log. The first entry will be the same as that written by <b>SetupWriteTextLog</b> and the second entry will log the error code and a user-friendly description of the error.

The log token, event category, and flags that a caller supplies affect the operation of <b>SetupWriteTextLogError</b> is the same manner as that described for <b>SetupWriteTextLog</b>.

<b>SetupWriteTextLogError</b> writes the first log entry in the following format: 

<i>entry-prefix</i>  <i>time_stamp category</i><i>indentation</i>  <i>formatted-message</i>

<b>SetupWriteTextLogError</b> writes the second log entry in the following format:

<i>entry-prefix</i>  <i>time_stamp</i>  <i>category</i> 
     <i>indentation</i>  
     <b>Error:</b> <i>error-numbererror-description</i>

Where:

<ul>
<li>
The <i>entry-prefix</i>, <i>time-stamp</i>, <i>category</i>, <i>indentation</i>, and <i>formatted-message</i> fields are the same as those described in <a href="https://docs.microsoft.com/windows-hardware/drivers/install/format-of-a-text-log-section-body">Format of a Text Log Section Body</a>.

</li>
<li>
The <i>error-number</i> field contains the error number.

</li>
<li>
The <i>error-description</i> field contains a user-friendly description of the error.

</li>
</ul>
For general information about writing log entries in the SetupAPI text logs, see <a href="https://docs.microsoft.com/windows-hardware/drivers/install/setupapi-logging--windows-vista-and-later-">SetupAPI Logging (Windows Vista)</a>. 

For more information about the operation of <b>SetupWriteTextLogError</b>, see <a href="https://docs.microsoft.com/windows-hardware/drivers/install/calling-setupwritetextlogerror">Calling SetupWriteTextLogError</a>. 

For more information about log tokens, see <a href="https://docs.microsoft.com/windows-hardware/drivers/install/log-tokens">Log Tokens</a>.

For more information about using log tokens, see <a href="https://docs.microsoft.com/windows-hardware/drivers/install/setting-and-getting-a-log-token-for-a-thread">Setting and Getting a Log Token for a Thread</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupgetthreadlogtoken">SetupGetThreadLogToken</a>



<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupwritetextlog">SetupWriteTextLog</a>
 

 

