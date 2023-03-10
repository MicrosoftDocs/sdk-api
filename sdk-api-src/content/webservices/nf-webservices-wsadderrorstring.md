---
UID: NF:webservices.WsAddErrorString
title: WsAddErrorString function (webservices.h)
description: Adds a specified error string to the error object.
helpviewer_keywords: ["WsAddErrorString","WsAddErrorString function [Web Services for Windows]","webservices/WsAddErrorString","wsw.wsadderrorstring"]
old-location: wsw\wsadderrorstring.htm
tech.root: wsw
ms.assetid: 5fdad296-5024-4360-b1c5-f0192929c612
ms.date: 12/05/2018
ms.keywords: WsAddErrorString, WsAddErrorString function [Web Services for Windows], webservices/WsAddErrorString, wsw.wsadderrorstring
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
 - WsAddErrorString
 - webservices/WsAddErrorString
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
 - WsAddErrorString
---

# WsAddErrorString function


## -description

Adds a specified error string to the error object.

## -parameters

### -param error [in]

Pointer to a <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> structure representing the error object to which to add the string.

### -param string [in]

The string to add.  The error object will
                    make a copy of the string.

## -returns

If the function succeeds, it returns NO_ERROR; otherwise, it returns an HRESULT error code.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

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

This function requires that the string be in the language specified by the LANGID of the 
                error object.  You can retrieve this LANGID value by calling the  <a href="/windows/desktop/api/webservices/nf-webservices-wsgeterrorproperty">WsGetErrorProperty</a> function with the WS_ERROR_PROPERTY_LANGID value of the <a href="/windows/desktop/api/webservices/ne-webservices-ws_error_property_id">WS_ERROR_PROPERTY_ID</a> enumeration.