---
UID: NS:webservices._WS_CERTIFICATE_VALIDATION_CALLBACK_CONTEXT
title: WS_CERTIFICATE_VALIDATION_CALLBACK_CONTEXT (webservices.h)
description: The WS_CERTIFICATE_VALIDATION_CALLBACK_CONTEXT structure contains the callback function and state for validating the certificate for an HTTP connection.
helpviewer_keywords: ["PWS_CERTIFICATE_VALIDATION_CALLBACK_CONTEXT","PWS_CERTIFICATE_VALIDATION_CALLBACK_CONTEXT structure pointer [Web Services for Windows]","WS_CERTIFICATE_VALIDATION_CALLBACK_CONTEXT","WS_CERTIFICATE_VALIDATION_CALLBACK_CONTEXT structure [Web Services for Windows]","webservices/PWS_CERTIFICATE_VALIDATION_CALLBACK_CONTEXT","webservices/WS_CERTIFICATE_VALIDATION_CALLBACK_CONTEXT","wsw.ws_certificate_validation_callback_context"]
old-location: wsw\ws_certificate_validation_callback_context.htm
tech.root: wsw
ms.assetid: 1D33A816-2580-4295-994D-6C6DFFBA7A0B
ms.date: 12/05/2018
ms.keywords: PWS_CERTIFICATE_VALIDATION_CALLBACK_CONTEXT, PWS_CERTIFICATE_VALIDATION_CALLBACK_CONTEXT structure pointer [Web Services for Windows], WS_CERTIFICATE_VALIDATION_CALLBACK_CONTEXT, WS_CERTIFICATE_VALIDATION_CALLBACK_CONTEXT structure [Web Services for Windows], webservices/PWS_CERTIFICATE_VALIDATION_CALLBACK_CONTEXT, webservices/WS_CERTIFICATE_VALIDATION_CALLBACK_CONTEXT, wsw.ws_certificate_validation_callback_context
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
req.typenames: WS_CERTIFICATE_VALIDATION_CALLBACK_CONTEXT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_CERTIFICATE_VALIDATION_CALLBACK_CONTEXT
 - webservices/_WS_CERTIFICATE_VALIDATION_CALLBACK_CONTEXT
 - WS_CERTIFICATE_VALIDATION_CALLBACK_CONTEXT
 - webservices/WS_CERTIFICATE_VALIDATION_CALLBACK_CONTEXT
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
 - WS_CERTIFICATE_VALIDATION_CALLBACK_CONTEXT
---

# WS_CERTIFICATE_VALIDATION_CALLBACK_CONTEXT structure


## -description

The <b>WS_CERTIFICATE_VALIDATION_CALLBACK_CONTEXT</b> structure contains the callback function and state for validating the certificate for an HTTP connection.

## -struct-fields

### -field callback

A <a href="/windows/desktop/api/webservices/nc-webservices-ws_certificate_validation_callback">WS_CERTIFICATE_VALIDATION_CALLBACK</a> callback that is an application specific callback for validating HTTP certificates.

### -field state

Application specific state that is made available to the callback when invoked.

## -see-also

<a href="/windows/desktop/api/webservices/nc-webservices-ws_certificate_validation_callback">WS_CERTIFICATE_VALIDATION_CALLBACK</a>