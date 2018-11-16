---
UID: NF:roerrorapi.RoTransformErrorW
title: RoTransformErrorW function
author: windows-sdk-content
description: Reports a transformed error and an informative string to an attached debugger.
old-location: winrt\rotransformerrorw.htm
tech.root: WinRT
ms.assetid: A13265FD-DC14-4552-A9FD-C954A7EA08C9
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: RoTransformErrorW, RoTransformErrorW function [Windows Runtime], WinRTTransformErrorW, roerrorapi/RoTransformErrorW, roerrorapi/WinRTTransformErrorW, winrt.rotransformerrorw, winrt.winrttransformerrorw
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: roerrorapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - roerrorapi.h
 - API-MS-Win-Core-WinRT-error-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-WinRT-error-l1-1-1.dll
api_name:
 - RoTransformErrorW
 - WinRTTransformErrorW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- RoTransformErrorW
: 
---

# RoTransformErrorW function


## -description


Reports a transformed error and an informative string to an attached debugger.


## -parameters




### -param oldError [in]

Type: <b>HRESULT</b>

The original error code associated with the error condition. 


### -param newError [in]

Type: <b>HRESULT</b>

The custom error code to associate with the error condition. If <i>oldError</i> and <i>newError</i>  are the same, or both are success codes, such as <b>S_OK</b>, the function has no effect and returns <b>FALSE</b>.


### -param cchMax [in]

Type: <b>UINT</b>

The maximum number of characters in <i>message</i>, excluding the terminating null character. If the value is 0, the string is read to the first null character or 512 characters, whichever is less. If <i>cchMax</i> is greater than 512, all characters after 512 are ignored.


### -param message [in]

Type: <b>PCWSTR</b>

An informative string to help developers to correct the reported error condition. The maximum length is 512 characters, including the trailing null character; longer strings are truncated.

If the string is empty, the function succeeds but no error information is reported. It is recommended that you always provide an informative string.

If <i>message</i> is <b>NULL</b>, the function succeeds and reports the generic string in Winerror.h if available or the generic string associated with E_FAIL.

This function does not support embedded null characters, so only the characters before the first null are reported.


## -returns



Type: <b>BOOL</b>

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
The  error message was reported successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
<i>message</i> is <b>NULL</b> or points to an empty string, or <i>oldError</i> and <i>newError</i> are the same, or both are success codes.

</td>
</tr>
</table>
 




## -remarks



Use the <b>RoTransformErrorW</b> function  to substitute a custom error code for an existing error condition. For example, if the current error condition is <b>E_FAIL</b>, you can substitute a more specific error code, such as  	<b>E_FILENOTFOUND</b> and report the transformed error to an attached debugger. 

The behavior of the  <b>RoTransformErrorW</b> function is otherwise the same as the <a href="https://msdn.microsoft.com/FC75DDA5-59BA-4CCF-93CC-8D0BB2AB415B">RoOriginateErrorW</a> function.

 If the <b>UseSetErrorInfo</b> flag is set by calling the <a href="https://msdn.microsoft.com/167C2EC9-9EA0-4E1D-840B-DAF5F47ED1FE">RoSetErrorReportingFlags</a> function, and the calling thread has been initialized in COM, the function creates an appropriate error object that supports <a href="https://msdn.microsoft.com/1af8d4bf-1217-44ca-b0dd-9a6feda16100">IRestrictedErrorInfo</a> and  associates it with the COM channel by calling <a href="https://msdn.microsoft.com/en-us/library/ms221409(v=VS.85).aspx">SetErrorInfo</a>.  If the thread has not been initialized into COM, the call will still succeed with no  error, but the error will not be associated with the COM channel.


<div class="alert"><b>Note</b>  This is no ANSI version of the <b>RoTransformErrorW</b> function. Message strings are required to be Unicode.</div>
<div> </div>





## -see-also




<a href="https://msdn.microsoft.com/345E1C4D-4A2F-4E18-9E70-4B8AE25FE8FD">RO_ERROR_REPORTING_FLAGS</a>



<a href="https://msdn.microsoft.com/0DCF6693-5066-46E3-A7F9-5CF0780FA87C">RoGetErrorReportingFlags</a>



<a href="https://msdn.microsoft.com/FC75DDA5-59BA-4CCF-93CC-8D0BB2AB415B">RoOriginateErrorW</a>



<a href="https://msdn.microsoft.com/167C2EC9-9EA0-4E1D-840B-DAF5F47ED1FE">RoSetErrorReportingFlags</a>



<a href="https://msdn.microsoft.com/B0921292-1EEA-4154-8AB4-B654A9B31DA6">RoTransformError</a>
 

 

