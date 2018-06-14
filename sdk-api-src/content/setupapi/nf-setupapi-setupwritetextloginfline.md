---
UID: NF:setupapi.SetupWriteTextLogInfLine
title: SetupWriteTextLogInfLine function
author: windows-sdk-content
description: The SetupWriteTextLogInfLine function writes a log entry in a SetupAPI text log that contains the text of a specified INF file line.
old-location: devinst\setupwritetextloginfline.htm
old-project: devinst
ms.assetid: 79386854-8b6b-4836-b8f3-d70657f6162c
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: SetupWriteTextLogInfLine, SetupWriteTextLogInfLine function [Device and Driver Installation], devinst.setupwritetextloginfline, setupapi/SetupWriteTextLogInfLine, setupapilog-ref_f6f9d000-dcfd-4dda-8a2c-bac81274a836.xml
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
 - Setupapi.dll
api_name:
 - SetupWriteTextLogInfLine
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# SetupWriteTextLogInfLine function


## -description


The <b>SetupWriteTextLogInfLine</b> function writes a log entry in a <a href="https://www.bing.com/search?q=SetupAPI+text+log">SetupAPI text log</a> that contains the text of a specified INF file line.


## -parameters




### -param LogToken [in]

A <a href="https://www.bing.com/search?q=log+token">log token</a> that is either a system-defined log token or was returned by <a href="https://msdn.microsoft.com/library/windows/hardware/ff552211">SetupGetThreadLogToken</a>.


### -param Flags [in]

A value of type DWORD that is a bitwise OR of flag values, which specify the following:

<ul>
<li>
The event level for the log entry. The event levels that can be specified for a log entry are the same as those that can be enabled for a text log. For a list of event level flags, see <a href="https://www.bing.com/search?q=Setting+the+Event+Level+for+a+SetupAPI+Text+Log">Setting the Event Level for a SetupAPI Text Log</a>. 

</li>
<li>
Whether to include a time stamp in the log entry. The time stamp flag value is TXTLOG_TIMESTAMP.

</li>
<li>
The change, if any, to the indentation depth of the section and the current log entry. For information about how to use the indentation flags, see <a href="https://www.bing.com/search?q=Writing+Indented+Log+Entries">Writing Indented Log Entries</a>.

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
The <i>entry-prefix</i> and <i>time-stamp</i> fields are the same as those described in <a href="https://www.bing.com/search?q=Format+of+a+Text+Log+Section+Body">Format of a Text Log Section Body</a>.

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
The log token and flags that a caller supplies affect the operation of <b>SetupWriteTextLogInfLine</b> in the same manner as that described for <a href="https://msdn.microsoft.com/library/windows/hardware/ff552218">SetupWriteTextLog</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff552232">SetupWriteTextLogError</a>. In addition, <b>SetupWriteTextLogInfLine</b> uses the <a href="https://www.bing.com/search?q=event+category">event category</a> TXTLOG_INF. 

For general information about writing log entries in the SetupAPI text logs, see <a href="https://www.bing.com/search?q=SetupAPI+Logging+(Windows+Vista)">SetupAPI Logging (Windows Vista)</a>. 

For more information about the operation of <b>SetupWriteTextLogInfLine</b>, see <a href="https://www.bing.com/search?q=Calling+SetupWriteTextLogInfLine">Calling SetupWriteTextLogInfLine</a>. 

For more information about the various types of log tokens, see <a href="https://www.bing.com/search?q=Log+Tokens">Log Tokens</a>.

For more information about using log tokens, see <a href="https://www.bing.com/search?q=Setting+and+Getting+a+Log+Token+for+a+Thread">Setting and Getting a Log Token for a Thread</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552211">SetupGetThreadLogToken</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552218">SetupWriteTextLog</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552232">SetupWriteTextLogError</a>
 

 

