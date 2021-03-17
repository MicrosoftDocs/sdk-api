---
UID: NS:webservices._WS_SERVICE_PROPERTY_CLOSE_CALLBACK
title: WS_SERVICE_PROPERTY_CLOSE_CALLBACK (webservices.h)
description: Specifies the callback which is called when a channel is about to be closed. See, WS_SERVICE_CLOSE_CHANNEL_CALLBACK for details.
helpviewer_keywords: ["WS_SERVICE_PROPERTY_CLOSE_CALLBACK","WS_SERVICE_PROPERTY_CLOSE_CALLBACK structure [Web Services for Windows]","webservices/WS_SERVICE_PROPERTY_CLOSE_CALLBACK","wsw.ws_service_property_close_callback"]
old-location: wsw\ws_service_property_close_callback.htm
tech.root: wsw
ms.assetid: 3806c87d-6abe-4dee-90cf-0a6d26826189
ms.date: 12/05/2018
ms.keywords: WS_SERVICE_PROPERTY_CLOSE_CALLBACK, WS_SERVICE_PROPERTY_CLOSE_CALLBACK structure [Web Services for Windows], webservices/WS_SERVICE_PROPERTY_CLOSE_CALLBACK, wsw.ws_service_property_close_callback
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WS_SERVICE_PROPERTY_CLOSE_CALLBACK
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_SERVICE_PROPERTY_CLOSE_CALLBACK
 - webservices/_WS_SERVICE_PROPERTY_CLOSE_CALLBACK
 - WS_SERVICE_PROPERTY_CLOSE_CALLBACK
 - webservices/WS_SERVICE_PROPERTY_CLOSE_CALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_SERVICE_PROPERTY_CLOSE_CALLBACK
---

# WS_SERVICE_PROPERTY_CLOSE_CALLBACK structure


## -description

Specifies the callback which is called when a channel is about to be closed. 
                See, <a href="/windows/desktop/api/webservices/nc-webservices-ws_service_close_channel_callback">WS_SERVICE_CLOSE_CHANNEL_CALLBACK</a> for details.

## -struct-fields

### -field callback

The close channel callback function reference.