---
UID: NF:webservices.WsCreateServiceHost
title: WsCreateServiceHost function (webservices.h)
description: Creates a service host for the specified endpoints.
helpviewer_keywords: ["WsCreateServiceHost","WsCreateServiceHost function [Web Services for Windows]","webservices/WsCreateServiceHost","wsw.wscreateservicehost"]
old-location: wsw\wscreateservicehost.htm
tech.root: wsw
ms.assetid: 412a262a-1706-4101-b154-1804408a5b9f
ms.date: 12/05/2018
ms.keywords: WsCreateServiceHost, WsCreateServiceHost function [Web Services for Windows], webservices/WsCreateServiceHost, wsw.wscreateservicehost
req.header: webservices.h
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
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WsCreateServiceHost
 - webservices/WsCreateServiceHost
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
 - WsCreateServiceHost
---

# WsCreateServiceHost function


## -description

Creates a <a href="/windows/desktop/wsw/service-host">service host</a> for the specified endpoints.

## -parameters

### -param endpoints

An array of  <a href="/windows/desktop/api/webservices/ns-webservices-ws_service_endpoint">WS_SERVICE_ENDPOINT</a> structures representing the service endpoints for which to create the service host.

### -param endpointCount [in]

The number of endpoints in the <i>endpoints</i> array.

### -param serviceProperties

An array of <a href="/windows/desktop/api/webservices/ns-webservices-ws_service_property">WS_SERVICE_PROPERTY</a> structures containing optional properties for the service host.

The value of this parameter may be <b>NULL</b>, in which case, the <i>servicePropertyCount</i> parameter must be 0 (zero).

### -param servicePropertyCount [in]

The number of properties in the <i>serviceProperties</i> array.

### -param serviceHost

On   success, a pointer that receives the address of the  <a href="/windows/desktop/wsw/ws-service-host">WS_SERVICE_HOST</a> structure representing the new service host.
                
When you no longer need this structure, you must free it by calling <a href="/windows/desktop/api/webservices/nf-webservices-wsfreeservicehost">WsFreeServiceHost</a>.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An invalid argument is specified for creating the service host.

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