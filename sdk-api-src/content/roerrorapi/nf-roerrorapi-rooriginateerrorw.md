---
UID: NF:roerrorapi.RoOriginateErrorW
title: RoOriginateErrorW function
description: Reports an error and an informative string to an attached debugger. (RoOriginateErrorW)
helpviewer_keywords: ["RoOriginateErrorW","RoOriginateErrorW function [Windows Runtime]","WinRTOriginateErrorW","roerrorapi/RoOriginateErrorW","roerrorapi/WinRTOriginateErrorW","winrt.rooriginateerrorw","winrt.winrtoriginateerrorw"]
old-location: winrt\rooriginateerrorw.htm
tech.root: WinRT
ms.assetid: FC75DDA5-59BA-4CCF-93CC-8D0BB2AB415B
ms.date: 12/5/2018
ms.keywords: RoOriginateErrorW, RoOriginateErrorW function [Windows Runtime], WinRTOriginateErrorW, roerrorapi/RoOriginateErrorW, roerrorapi/WinRTOriginateErrorW, winrt.rooriginateerrorw, winrt.winrtoriginateerrorw
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
req.lib: RuntimeObject.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - RoOriginateErrorW
 - roerrorapi/RoOriginateErrorW
dev_langs:
 - c++
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

 If the <b>UseSetErrorInfo</b> flag is set by calling the <a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-roseterrorreportingflags">RoSetErrorReportingFlags</a> function, and the calling thread has been initialized in COM, the function creates an appropriate error object that supports <a href="/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-irestrictederrorinfo">IRestrictedErrorInfo</a> and  associates it with the COM channel by calling <a href="/windows/win32/api/oleauto/nf-oleauto-seterrorinfo">SetErrorInfo</a>.  If the thread has not been initialized into COM, the call will still succeed with no  error, but the error will not be associated with the COM channel.

<div class="alert"><b>Note</b>  This is no ANSI version of the <b>RoOriginateErrorW</b> function. Message strings are required to be Unicode. </div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/roerrorapi/ne-roerrorapi-roerrorreportingflags">RO_ERROR_REPORTING_FLAGS</a>



<a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-rogeterrorreportingflags">RoGetErrorReportingFlags</a>



<a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-rooriginateerror">RoOriginateError</a>



<a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-roseterrorreportingflags">RoSetErrorReportingFlags</a>



<a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-rotransformerror">RoTransformErrorW</a>
