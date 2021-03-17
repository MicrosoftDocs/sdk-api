---
UID: NF:roerrorapi.RoOriginateLanguageException
title: RoOriginateLanguageException function
description: Reports an error, an informative string, and an error object to an attached debugger.
helpviewer_keywords: ["RoOriginateLanguageException","RoOriginateLanguageException function [Windows Runtime]","roerrorapi/RoOriginateLanguageException","winrt.rooriginatelanguageexception"]
old-location: winrt\rooriginatelanguageexception.htm
tech.root: WinRT
ms.assetid: 573A9209-31EF-4FD4-A504-16795BA42337
ms.date: 12/5/2018
ms.keywords: RoOriginateLanguageException, RoOriginateLanguageException function [Windows Runtime], roerrorapi/RoOriginateLanguageException, winrt.rooriginatelanguageexception
req.header: roerrorapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
req.dll: ComBase.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - RoOriginateLanguageException
 - roerrorapi/RoOriginateLanguageException
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ComBase.dll
 - API-MS-Win-Core-WinRT-error-l1-1-1.dll
api_name:
 - RoOriginateLanguageException
---

# RoOriginateLanguageException function


## -description

Reports an error, an informative string, and an error object to an attached debugger.

## -parameters

### -param error [in]

The error code associated with the error condition. If <i>error</i> is a success code, like <b>S_OK</b>, the function has no effect and returns <b>FALSE</b>. This behavior enables calling the function when no error has occurred without causing an unwanted error message.

### -param message [in, optional]

An informative string to help developers to correct the reported error condition. The maximum length is 512 characters, including the trailing <b>NUL</b> character; longer strings are truncated.

If the string is empty, the function succeeds but no error information is reported. It is recommended that you always provide an informative string.

If <i>message</i> is <b>NULL</b>, the function succeeds and reports the generic string in Winerror.h if available or the generic string associated with <b>E_FAIL</b>.

This function does not support embedded <b>NUL</b> characters, so only the characters before the first <b>NUL</b> are reported.

The <i>message</i> string should be localized.

### -param languageException [in]

An error object that's apartment-agile, in-proc, and marshal-by-value across processes. This object should implement <a href="/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-ilanguageexceptionstackbacktrace">ILanguageExceptionStackBackTrace</a> and <a href="/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-ilanguageexceptiontransform">ILanguageExceptionTransform</a> if necessary.

## -returns

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

The <b>RoOriginateLanguageException</b>  function behaves like <a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-rooriginateerror">RoOriginateError</a> but takes another parameter that stores extra information about the error. Language projections use this function to store exception information alongside the COM error information. Language projections need to create an <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> object that contains all the information necessary recreate it the exception a later point.

The error object must be apartment-agile, in-proc, and marshal-by-value across processes. The reason for this restriction is that the thread from which the error object is originated may no longer exist, for example due to a <a href="/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize">CoUninitialize</a> call, by the time the error information is retrieved.

## -see-also

<a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-rooriginateerror">RoOriginateError</a>