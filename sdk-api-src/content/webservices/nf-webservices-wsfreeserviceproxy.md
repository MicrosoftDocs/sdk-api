---
UID: NF:webservices.WsFreeServiceProxy
title: WsFreeServiceProxy function (webservices.h)
description: Releases the memory associated with a Service Proxy resource.
helpviewer_keywords: ["WsFreeServiceProxy","WsFreeServiceProxy function [Web Services for Windows]","webservices/WsFreeServiceProxy","wsw.wsfreeserviceproxy"]
old-location: wsw\wsfreeserviceproxy.htm
tech.root: wsw
ms.assetid: fb200cf8-c1d4-4a97-afef-f7c4ed5efb10
ms.date: 12/05/2018
ms.keywords: WsFreeServiceProxy, WsFreeServiceProxy function [Web Services for Windows], webservices/WsFreeServiceProxy, wsw.wsfreeserviceproxy
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
 - WsFreeServiceProxy
 - webservices/WsFreeServiceProxy
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
 - WsFreeServiceProxy
---

# WsFreeServiceProxy function


## -description

Releases the memory associated with  a Service Proxy resource.

## -parameters

### -param serviceProxy [in]

A pointer to the <b>Service Proxy</b> to release.  The pointer must reference a valid <a href="/windows/desktop/wsw/ws-service-proxy">WS_SERVICE_PROXY</a> object
                    returned by <a href="/windows/desktop/api/webservices/nf-webservices-wscreateserviceproxy">WsCreateServiceProxy</a>. The referenced value may not be <b>NULL</b>.

## -remarks

For details of when it is allowed to call this function, see <a href="/windows/desktop/wsw/service-proxy">Service Proxy</a> .