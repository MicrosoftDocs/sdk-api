---
UID: NF:webservices.WsCall
title: WsCall function (webservices.h)
description: Used internally by the service proxy to format the specified arguments according to the specified metadata and send them in a message. The application should never call this function directly.
helpviewer_keywords: ["WsCall","WsCall function [Web Services for Windows]","webservices/WsCall","wsw.wscall"]
old-location: wsw\wscall.htm
tech.root: wsw
ms.assetid: 300d25b7-6742-4bed-9786-6c599981ec22
ms.date: 12/05/2018
ms.keywords: WsCall, WsCall function [Web Services for Windows], webservices/WsCall, wsw.wscall
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
 - WsCall
 - webservices/WsCall
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
 - WsCall
---

# WsCall function


## -description

Used internally by the <a href="/windows/desktop/wsw/service-proxy">service proxy</a>  to format the specified arguments according to the specified metadata and send them in a message. The application should 
                never call this function directly.

## -parameters

### -param serviceProxy [in]

Pointer to a WS_SERVICE_PROXY structure representing the service proxy.

### -param operation [in]

Pointer to a <a href="/windows/desktop/api/webservices/ns-webservices-ws_operation_description">WS_OPERATION_DESCRIPTION</a> structure containing the metadata for the call.

### -param arguments [in, optional]

An array of pointers to the individual arguments for the service operation being represented by the <i>operation</i> parameter.

The number of elements must correspond to the number of parameters specified as part of WS_OPERATION_DESCRIPTION in
                   the operation parameter.

### -param heap [in]

Pointer to a <a href="/windows/desktop/wsw/ws-heap">WS_HEAP</a> structure representing the <a href="/windows/desktop/wsw/heap">heap</a> from which memory is allocated for the call.

### -param callProperties

An array of <a href="/windows/desktop/api/webservices/ns-webservices-ws_call_property">WS_CALL_PROPERTY</a> structures containing the call properties.

### -param callPropertyCount [in]

The number of properties in the call properties array.

### -param asyncContext [in, optional]

Pointer to information for invoking the function asynchronously. Pass <b>NULL</b> to invoke the function synchronously.

### -param error [in, optional]

Pointer to a <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> structure  that receives additional error information if the function fails.

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
<dt><b>WS_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The operation is not allowed due to the current state of the object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_QUOTA_EXCEEDED</b></dt>
</dl>
</td>
<td width="60%">
A quota was exceeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_OPERATION_ABANDONED</b></dt>
</dl>
</td>
<td width="60%">
The operation was abandoned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_OPERATION_TIMED_OUT</b></dt>
</dl>
</td>
<td width="60%">
The operation did not complete within the time allotted.

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
<dt><b>WS_S_ASYNC</b></dt>
</dl>
</td>
<td width="60%">
The asynchronous operation is still pending.
                

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