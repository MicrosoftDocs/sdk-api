---
UID: NC:webservices.WS_SERVICE_SECURITY_CALLBACK
title: WS_SERVICE_SECURITY_CALLBACK (webservices.h)
description: Invoked when headers of the incoming message are received and the body is not processed.
helpviewer_keywords: ["WS_SERVICE_SECURITY_CALLBACK","WS_SERVICE_SECURITY_CALLBACK callback","WS_SERVICE_SECURITY_CALLBACK callback function [Web Services for Windows]","webservices/WS_SERVICE_SECURITY_CALLBACK","wsw.ws_service_security_callback"]
old-location: wsw\ws_service_security_callback.htm
tech.root: wsw
ms.assetid: 0fa127ea-a715-4f21-8b49-3c2705c2bf5d
ms.date: 12/05/2018
ms.keywords: WS_SERVICE_SECURITY_CALLBACK, WS_SERVICE_SECURITY_CALLBACK callback, WS_SERVICE_SECURITY_CALLBACK callback function [Web Services for Windows], webservices/WS_SERVICE_SECURITY_CALLBACK, wsw.ws_service_security_callback
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_SERVICE_SECURITY_CALLBACK
 - webservices/WS_SERVICE_SECURITY_CALLBACK
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
 - WS_SERVICE_SECURITY_CALLBACK
---

# WS_SERVICE_SECURITY_CALLBACK callback function


## -description

Invoked when headers of the incoming message 
                are received and the body is not processed.

## -parameters

### -param context [in]

The incoming message with headers only.

### -param authorized [out]

Set to <b>TRUE</b>, if authorization succeeded, <b>FALSE</b> if authorization failed.

### -param error [in, optional]

Specifies where additional error information should be stored if the function fails.

## -returns

This callback function does not return a value.

