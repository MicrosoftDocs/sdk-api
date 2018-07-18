---
UID: NF:roerrorapi.RoOriginateErrorW
title: RoOriginateErrorW function
author: windows-sdk-content
description: Reports an error and an informative string to an attached debugger.
old-location: winrt\rooriginateerrorw.htm
old-project: WinRT
ms.assetid: FC75DDA5-59BA-4CCF-93CC-8D0BB2AB415B
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: RoOriginateErrorW, RoOriginateErrorW function [Windows Runtime], WinRTOriginateErrorW, roerrorapi/RoOriginateErrorW, roerrorapi/WinRTOriginateErrorW, winrt.rooriginateerrorw, winrt.winrtoriginateerrorw
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: RO_ERROR_REPORTING_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - RuntimeObject.lib
 - RuntimeObject.dll
 - API-MS-Win-Core-WinRT-error-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-WinRT-error-l1-1-1.dll
api_name:
 - RoOriginateErrorW
 - WinRTOriginateErrorW
product: Windows
targetos: Windows
req.lib: RuntimeObject.lib
req.dll: 
req.irql: 
req.product: ADAM
---

# RoOriginateErrorW function


## -description


Reports an error and an informative string to an attached debugger.


## -parameters




### -param error [in]

Type: <b>HRESULT</b>

The error code associated with the error condition. If <i>error</i> is a success code, such as <b>S_OK</b>, the function has no effect and returns <b>FALSE</b>. This behavior enables calling the function when no error has occurred without causing an unwanted error message.


### -param cchMax [in]

Type: <b>UINT</b>

The maximum number of characters in <i>message</i>, excluding the terminating <b>NUL</b> character. If the value is 0, the string is read to the first <b>NUL</b> character or 512 characters, whichever is less. If <i>cchMax</i> is greater than 512, all characters after 512 are ignored.


### -param message [in]

Type: <b>PCWSTR</b>

An informative string to help developers to correct the reported error condition. The maximum length is 512 characters, including the trailing <b>NUL</b> character; longer strings are truncated.

If the string is empty, the function succeeds but no error information is reported. It is recommended that you always provide an informative string.

If <i>message</i> is <b>NULL</b>, the function succeeds and reports the generic string in Winerror.h if available or the generic string associated with <b>E_FAIL</b>.

This function does not support embedded <b>NUL</b> characters, so only the characters before the first <b>NUL</b> are reported.

The <i>message</i> string should be localized.


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
<i>message</i> is <b>NULL</b> or points to an empty string, or <i>error</i> is a success code.

</td>
</tr>
</table>
 




## -remarks



Use the <b>RoOriginateErrorW</b> function  to report an error condition and a corresponding message to a debugger. This function does not perform logging or event tracing.

The error is communicated to the debugger by raising a structured exception.  This exception is caught by the attached debugger, and the exception parameters contain both the error and the <i>message</i> string.  The debugger may display these parameters to the user.

Depending on the current configuration of the debugger, the <b>RoOriginateErrorW</b> function may cause execution to halt in the debugger at the site of the exception.

 If the <b>UseSetErrorInfo</b> flag is set by calling the <a href="https://msdn.microsoft.com/167C2EC9-9EA0-4E1D-840B-DAF5F47ED1FE">RoSetErrorReportingFlags</a> function, and the calling thread has been initialized in COM, the function creates an appropriate error object that supports <a href="https://msdn.microsoft.com/1af8d4bf-1217-44ca-b0dd-9a6feda16100">IRestrictedErrorInfo</a> and  associates it with the COM channel by calling <a href="https://msdn.microsoft.com/library/ms221409(v=VS.85).aspx">SetErrorInfo</a>.  If the thread has not been initialized into COM, the call will still succeed with no  error, but the error will not be associated with the COM channel.

<div class="alert"><b>Note</b>  This is no ANSI version of the <b>RoOriginateErrorW</b> function. Message strings are required to be Unicode. </div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/345E1C4D-4A2F-4E18-9E70-4B8AE25FE8FD">RO_ERROR_REPORTING_FLAGS</a>



<a href="https://msdn.microsoft.com/0DCF6693-5066-46E3-A7F9-5CF0780FA87C">RoGetErrorReportingFlags</a>



<a href="https://msdn.microsoft.com/ED647880-5A18-4F75-B7E5-3B9BF36229D3">RoOriginateError</a>



<a href="https://msdn.microsoft.com/167C2EC9-9EA0-4E1D-840B-DAF5F47ED1FE">RoSetErrorReportingFlags</a>



<a href="https://msdn.microsoft.com/B0921292-1EEA-4154-8AB4-B654A9B31DA6">RoTransformErrorW</a>
 

 

