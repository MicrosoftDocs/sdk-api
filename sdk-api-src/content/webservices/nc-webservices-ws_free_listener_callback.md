---
UID: NC:webservices.WS_FREE_LISTENER_CALLBACK
title: WS_FREE_LISTENER_CALLBACK (webservices.h)
description: Handles the WsFreeListener call for a WS_CUSTOM_CHANNEL_BINDING.
helpviewer_keywords: ["WS_FREE_LISTENER_CALLBACK","WS_FREE_LISTENER_CALLBACK callback","WS_FREE_LISTENER_CALLBACK callback function [Web Services for Windows]","webservices/WS_FREE_LISTENER_CALLBACK","wsw.ws_free_listener_callback"]
old-location: wsw\ws_free_listener_callback.htm
tech.root: wsw
ms.assetid: fd60ae42-5b3f-4482-b785-541f7379ab3e
ms.date: 12/05/2018
ms.keywords: WS_FREE_LISTENER_CALLBACK, WS_FREE_LISTENER_CALLBACK callback, WS_FREE_LISTENER_CALLBACK callback function [Web Services for Windows], webservices/WS_FREE_LISTENER_CALLBACK, wsw.ws_free_listener_callback
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_FREE_LISTENER_CALLBACK
 - webservices/WS_FREE_LISTENER_CALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - WebServices.h
api_name:
 - WS_FREE_LISTENER_CALLBACK
---

# WS_FREE_LISTENER_CALLBACK callback function


## -description

Handles the <a href="/windows/desktop/api/webservices/nf-webservices-wsfreelistener">WsFreeListener</a> call
                for a <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_binding">WS_CUSTOM_CHANNEL_BINDING</a>.

## -parameters

### -param listenerInstance [in]

The pointer to the state specific to this listener instance,
                    as created by the <a href="/windows/desktop/api/webservices/nc-webservices-ws_create_listener_callback">WS_CREATE_LISTENER_CALLBACK</a>.
                

The callback should free this pointer.

## -remarks

See <a href="/windows/desktop/api/webservices/nf-webservices-wsopenlistener">WsOpenListener</a> for information about the contract
                of this API.
