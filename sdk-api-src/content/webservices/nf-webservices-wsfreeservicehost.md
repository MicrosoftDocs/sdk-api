---
UID: NF:webservices.WsFreeServiceHost
title: WsFreeServiceHost function (webservices.h)
description: Releases the memory associated with a Service Host object.
helpviewer_keywords: ["WsFreeServiceHost","WsFreeServiceHost function [Web Services for Windows]","webservices/WsFreeServiceHost","wsw.wsfreeservicehost"]
old-location: wsw\wsfreeservicehost.htm
tech.root: wsw
ms.assetid: 5362d8a4-8b38-462a-a7c1-9cde19abee1e
ms.date: 12/05/2018
ms.keywords: WsFreeServiceHost, WsFreeServiceHost function [Web Services for Windows], webservices/WsFreeServiceHost, wsw.wsfreeservicehost
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
 - WsFreeServiceHost
 - webservices/WsFreeServiceHost
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
 - WsFreeServiceHost
---

# WsFreeServiceHost function


## -description

Releases the memory associated with  a <a href="/windows/desktop/wsw/service-host">Service Host</a> object.

## -parameters

### -param serviceHost [in]

A pointer to the <b>Service Host</b> object to release.  The pointer must reference a valid <a href="/windows/desktop/wsw/ws-service-host">WS_SERVICE_HOST</a> object
                    returned by <a href="/windows/desktop/api/webservices/nf-webservices-wscreateservicehost">WsCreateServiceHost</a> and the referenced <b>Service Host</b> value may not be <b>NULL</b>.