---
UID: NF:evntrace.TraceQueryInformation
title: TraceQueryInformation function (evntrace.h)
description: Queries event tracing session settings for the specified information class.helpviewer_keywords: ["TraceQueryInformation","TraceQueryInformation function [ETW]","etw.tracequeryinformation","evntrace/TraceQueryInformation"]
old-location: etw\tracequeryinformation.htm
tech.root: ETW
ms.assetid: 3CC91F7C-7F82-4B3B-AA50-FE03CFEC0278
ms.date: 12/05/2018
ms.keywords: TraceQueryInformation, TraceQueryInformation function [ETW], etw.tracequeryinformation, evntrace/TraceQueryInformation
f1_keywords:
- evntrace/TraceQueryInformation
dev_langs:
- c++
req.header: evntrace.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Sechost.lib on Windows 8.1 and Windows Server 2012 R2; Advapi32.lib on Windows 8 and Windows Server 2012
req.dll: Sechost.dll on Windows 8.1 and Windows Server 2012 R2; Advapi32.dll on Windows 8 and Windows Server 2012
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Sechost.dll
- Advapi32.dll
- API-MS-Win-Eventing-Controller-l1-1-0.dll
- KernelBase.dll
api_name:
- TraceQueryInformation
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TraceQueryInformation function


## -description


The <b>TraceQueryInformation</b> function 
    queries event tracing session settings for the specified information class.


## -parameters




### -param SessionHandle [in]

A handle of the event tracing session that wants to capture the specified information. The 
      <a href="https://docs.microsoft.com/windows/desktop/ETW/starttrace">StartTrace</a> function returns this handle. 


### -param InformationClass [in]

The information class to query. The information that the class captures is included in the extended data 
      section of the event. For a list of information classes that you can query, see the 
      <a href="https://docs.microsoft.com/windows/desktop/ETW/trace-info-class">TRACE_QUERY_INFO_CLASS</a> enumeration.


### -param TraceInformation [out]

A pointer to a buffer to receive the returned information class specific data. The information class 
      determines the contents of this parameter. For example, for the <b>TraceStackTracingInfo</b> 
      information class, this parameter is an array of 
      <a href="https://docs.microsoft.com/windows/desktop/ETW/classic-event-id">CLASSIC_EVENT_ID</a> structures. The structures specify 
      the event GUIDs for which stack tracing is enabled. The array is limited to 256 elements.


### -param InformationLength [in]

The size, in bytes, of the data returned in the <i>TraceInformation</i> buffer. If the 
      function fails, this value indicates the required size of the <i>TraceInformation</i> buffer 
      that is needed.


### -param ReturnLength [out, optional]

A pointer a value that receives the size, in bytes, of the specific data returned in the 
      <i>TraceInformation</i> buffer.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_LENGTH</b></dt>
</dl>
</td>
<td width="60%">
The program issued a command but the command length is incorrect. This error is returned if the 
        <i>InformationLength</i> parameter is less than a minimum size.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The parameter is incorrect. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The request is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
Use <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to obtain the message string 
        for the returned error.

</td>
</tr>
</table>
 




## -remarks



The <b>TraceQueryInformation</b> function queries 
     event tracing session settings for the specified information class. Call this function after calling 
     <a href="https://docs.microsoft.com/windows/desktop/ETW/starttrace">StartTrace</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/ETW/trace-info-class">TRACE_QUERY_INFO_CLASS</a>



<a href="https://docs.microsoft.com/windows/desktop/ETW/tracesetinformation">TraceSetInformation</a>
 

 

