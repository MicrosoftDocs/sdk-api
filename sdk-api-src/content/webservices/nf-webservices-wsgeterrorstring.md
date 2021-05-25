---
UID: NF:webservices.WsGetErrorString
title: WsGetErrorString function (webservices.h)
description: Retrieves an error string from an error object.
helpviewer_keywords: ["WsGetErrorString","WsGetErrorString function [Web Services for Windows]","webservices/WsGetErrorString","wsw.wsgeterrorstring"]
old-location: wsw\wsgeterrorstring.htm
tech.root: wsw
ms.assetid: 711c14b4-6a74-4860-a9cc-7b8673dc1a28
ms.date: 12/05/2018
ms.keywords: WsGetErrorString, WsGetErrorString function [Web Services for Windows], webservices/WsGetErrorString, wsw.wsgeterrorstring
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WsGetErrorString
 - webservices/WsGetErrorString
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsGetErrorString
---

# WsGetErrorString function


## -description

Retrieves an error string from an error object.

## -parameters

### -param error [in]

The error object containing the string.

### -param index [in]

The zero-based index identifying the string to retrieve.  The first
                    error string (index 0) will be the string most recently added to the
                    error object (using <a href="/windows/desktop/api/webservices/nf-webservices-wsadderrorstring">WsAddErrorString</a>). When 
                    <a href="/windows/desktop/api/webservices/ne-webservices-ws_error_property_id">WS_ERROR_PROPERTY_ORIGINAL_ERROR_CODE</a> is presented in the 
                    error object, the corresponding error text will be available in the last index.
                

The number of errors can be retrieved using <a href="/windows/desktop/api/webservices/ne-webservices-ws_error_property_id">WS_ERROR_PROPERTY_STRING_COUNT</a>.

### -param string [out]

The returned string.  The string is valid until <a href="/windows/desktop/api/webservices/nf-webservices-wsreseterror">WsResetError</a> or <a href="/windows/desktop/api/webservices/nf-webservices-wsfreeerror">WsFreeError</a> is called.
                

The string is not zero terminated.

## -returns

This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more arguments are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b> Other Errors </b></dt>
</dl>
</td>
<td width="60%">
This function may return other errors not listed above.

</td>
</tr>
</table>

## -remarks

The string is in the language specified by the LANGID property of
                the error object.  This can be retrieved using <a href="/windows/desktop/api/webservices/nf-webservices-wsgeterrorproperty">WsGetErrorProperty</a> with <a href="/windows/desktop/api/webservices/ne-webservices-ws_error_property_id">WS_ERROR_PROPERTY_LANGID</a>.