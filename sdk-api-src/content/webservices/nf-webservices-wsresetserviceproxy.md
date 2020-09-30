---
UID: NF:webservices.WsResetServiceProxy
title: WsResetServiceProxy function (webservices.h)
description: Resets service proxy.
helpviewer_keywords: ["WsResetServiceProxy","WsResetServiceProxy function [Web Services for Windows]","webservices/WsResetServiceProxy","wsw.wsresetserviceproxy"]
old-location: wsw\wsresetserviceproxy.htm
tech.root: wsw
ms.assetid: 6a99c958-92f9-4487-8768-3265dab7f0ea
ms.date: 12/05/2018
ms.keywords: WsResetServiceProxy, WsResetServiceProxy function [Web Services for Windows], webservices/WsResetServiceProxy, wsw.wsresetserviceproxy
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
 - WsResetServiceProxy
 - webservices/WsResetServiceProxy
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
 - WsResetServiceProxy
---

# WsResetServiceProxy function


## -description

Resets service proxy.

WsResetServiceProxy provides a convenient way to reuse the service proxy. 
                Once the proxy is <a href="/windows/desktop/api/webservices/ne-webservices-ws_service_proxy_state">closed</a>,
                the application can call WsResetServiceProxy to reuse it.
            

Reusing the service proxy is helpful in scenarios where an application connects 
                to the same service time and time again. The cost of initialization is only paid 
                once during the initial creation of the service proxy.

## -parameters

### -param serviceProxy [in]

The service proxy.

### -param error [in, optional]

Specifies where additional error information should be stored if the function fails.

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
<dt><b>WS_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The serviceProxy was in an inappropriate state.

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
</table>