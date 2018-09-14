---
UID: NF:evntrace.TraceSetInformation
title: TraceSetInformation function
author: windows-sdk-content
description: Enables or disables event tracing session settings for the specified information class.
old-location: etw\tracesetinformation.htm
tech.root: ETW
ms.assetid: f4cdbe32-6885-4844-add5-560961c3dd1d
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: TraceSetInformation, TraceSetInformation function [ETW], etw.tracesetinformation, evntrace/TraceSetInformation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: evntrace.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Sechost.lib on Windows 8.1 and Windows Server 2012 R2; Advapi32.lib on Windows 8, Windows Server 2012, Windows 7 and Windows Server 2008 R2
req.dll: Sechost.dll on Windows 8.1 and Windows Server 2012 R2; Advapi32.dll on Windows 8, Windows Server 2012, Windows 7 and Windows Server 2008 R2
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Sechost.dll
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvAPI32-l2-1-1.dll
 - API-MS-Win-Eventing-Controller-l1-1-0.dll
 - KernelBase.dll
api_name:
 - TraceSetInformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TraceSetInformation function


## -description


The <b>TraceSetInformation</b> function 
    enables or disables event tracing session settings for  the specified information class.


## -parameters




### -param SessionHandle [in]

A handle of the event tracing session that wants to capture the specified information. The 
<a href="https://msdn.microsoft.com/c040514a-733d-44b9-8300-a8341d2630b3">StartTrace</a> function returns this handle. 


### -param InformationClass [in]

The information class to enable or disable. The information that the class captures is included in the 
      extended data section of the event. For a list of information classes that you can enable, see the 
      <a href="https://msdn.microsoft.com/b163e120-454a-48ba-93a9-71351fc3f2c2">TRACE_INFO_CLASS</a> enumeration.


### -param TraceInformation [in]

A pointer to information class specific data; the information class determines the contents of this 
      parameter. For example, for the <b>TraceStackTracingInfo</b> information class, this 
      parameter is an array of <a href="https://msdn.microsoft.com/cbd77002-466b-40e6-85a5-cd872aef7d51">CLASSIC_EVENT_ID</a> structures. 
      The structures specify the event GUIDs for which stack tracing is enabled. The array is limited to 256 
      elements.


### -param InformationLength [in]

The size, in bytes, of the data in the <i>TraceInformation</i> buffer. 


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
Use 
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> to obtain the message string for the returned error.

</td>
</tr>
</table>
 




## -remarks



Call this function after calling <a href="https://msdn.microsoft.com/c040514a-733d-44b9-8300-a8341d2630b3">StartTrace</a>.

If the <i>InformationClass</i> parameter is set to 
    <b>TraceStackTracingInfo</b>, calling this function enables stack tracing of the specified 
    kernel events. Subsequent calls to this function overwrites the previous list of kernel events for which stack 
    tracing is enabled. To disable stack tracing, call this function with <i>InformationClass</i> 
    set to <b>TraceStackTracingInfo</b> and <i>InformationLength</i> set to 
    0.

The extended data section of the event will include the call stack. The 
    <a href="https://msdn.microsoft.com/05117bd6-a39c-42f3-8aed-c6f758f946c6">StackWalk_Event</a> MOF class defines the layout of the 
    extended data.

Typically, on 64-bit computers, you cannot capture the kernel stack in certain contexts when page faults are 
     not allowed. To enable walking the kernel stack on x64, set the 
     <b>DisablePagingExecutive</b> Memory Management registry value to 1. The 
     <b>DisablePagingExecutive</b> registry value is located under the following registry 
     key:


<b>HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\Session Manager\Memory Management</b>



You should consider the cost of setting this registry value before doing so.




## -see-also




<a href="https://msdn.microsoft.com/b163e120-454a-48ba-93a9-71351fc3f2c2">TRACE_INFO_CLASS</a>



<a href="https://msdn.microsoft.com/3CC91F7C-7F82-4B3B-AA50-FE03CFEC0278">TraceQueryInformation</a>
 

 

