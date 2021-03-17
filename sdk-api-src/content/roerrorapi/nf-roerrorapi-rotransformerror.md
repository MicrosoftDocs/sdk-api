---
UID: NF:roerrorapi.RoTransformError
title: RoTransformError function
description: Reports a modified error and an informative string to an attached debugger.
helpviewer_keywords: ["RoTransformError","RoTransformError function [Windows Runtime]","WinRTTransformError","roerrorapi/RoTransformError","roerrorapi/WinRTTransformError","winrt.rotransformerror","winrt.winrttransformerror"]
old-location: winrt\rotransformerror.htm
tech.root: WinRT
ms.assetid: B0921292-1EEA-4154-8AB4-B654A9B31DA6
ms.date: 12/5/2018
ms.keywords: RoTransformError, RoTransformError function [Windows Runtime], WinRTTransformError, roerrorapi/RoTransformError, roerrorapi/WinRTTransformError, winrt.rotransformerror, winrt.winrttransformerror
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
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - RoTransformError
 - roerrorapi/RoTransformError
dev_langs:
 - c++
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
 - RoTransformError
 - WinRTTransformError
---

# RoTransformError function


## -description

Reports a modified error and an informative string to an attached debugger.

## -parameters

### -param oldError [in]

Type: <b>HRESULT</b>

The original error code associated with the error condition.

### -param newError [in]

Type: <b>HRESULT</b>

A different  error code to associate with the error condition. If <i>oldError</i> and <i>newError</i>  are the same, or both are success codes, such as <b>S_OK</b>, the function has no effect and returns <b>FALSE</b>.

### -param message [in]

Type: <b><a href="/windows/desktop/WinRT/hstring">HSTRING</a></b>

An informative string to help developers to correct the reported error condition. The maximum length is 512 characters, including the trailing null character; longer strings are truncated.

If the string is empty, the function succeeds but no error information is reported. It is recommended that you always provide an informative string.

If <i>message</i> is <b>NULL</b>, the function succeeds and reports the generic string in Winerror.h if available or the generic string associated with E_FAIL.

Although the <i>message</i> string is an <a href="/windows/desktop/WinRT/hstring">HSTRING</a>, the <b>RoTransformError</b> function  does not support embedded null characters, so only the characters before the first null are reported.

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

Use the <b>RoTransformError</b> function  to substitute a custom error code for an existing error condition. For example, if the current error condition is <b>E_FAIL</b>, you can substitute a more specific error code, such as  	<b>E_FILENOTFOUND</b>, and report the transformed error to an attached debugger. 

The behavior of the  <b>RoTransformError</b> function is otherwise the same as the <a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-rotransformerrorw">RoTransformErrorW</a> function.

 If the <b>UseSetErrorInfo</b> flag is set by calling the <a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-roseterrorreportingflags">RoSetErrorReportingFlags</a> function, and the calling thread has been initialized in COM, the function creates an appropriate error object that supports <a href="/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-irestrictederrorinfo">IRestrictedErrorInfo</a> and  associates it with the COM channel by calling <a href="/windows/win32/api/oleauto/nf-oleauto-seterrorinfo">SetErrorInfo</a>.  If the thread has not been initialized into COM, the call will still succeed with no  error, but the error will not be associated with the COM channel.

## -see-also

<a href="/windows/desktop/api/roerrorapi/ne-roerrorapi-roerrorreportingflags">RO_ERROR_REPORTING_FLAGS</a>



<a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-rogeterrorreportingflags">RoGetErrorReportingFlags</a>



<a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-rooriginateerror">RoOriginateError</a>



<a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-roseterrorreportingflags">RoSetErrorReportingFlags</a>



<a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-rotransformerrorw">RoTransformErrorW</a>