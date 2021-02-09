---
UID: NC:webservices.WS_PUSH_BYTES_CALLBACK
title: WS_PUSH_BYTES_CALLBACK (webservices.h)
description: Used by the WsPushBytes function to request that data be written.
helpviewer_keywords: ["WS_PUSH_BYTES_CALLBACK","WS_PUSH_BYTES_CALLBACK callback","WS_PUSH_BYTES_CALLBACK callback function [Web Services for Windows]","webservices/WS_PUSH_BYTES_CALLBACK","wsw.ws_push_bytes_callback"]
old-location: wsw\ws_push_bytes_callback.htm
tech.root: wsw
ms.assetid: e2f88488-94b7-41c8-95ae-9c409b132466
ms.date: 12/05/2018
ms.keywords: WS_PUSH_BYTES_CALLBACK, WS_PUSH_BYTES_CALLBACK callback, WS_PUSH_BYTES_CALLBACK callback function [Web Services for Windows], webservices/WS_PUSH_BYTES_CALLBACK, wsw.ws_push_bytes_callback
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
 - WS_PUSH_BYTES_CALLBACK
 - webservices/WS_PUSH_BYTES_CALLBACK
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
 - WS_PUSH_BYTES_CALLBACK
---

# WS_PUSH_BYTES_CALLBACK callback function


## -description

Used by the <a href="/windows/desktop/api/webservices/nf-webservices-wspushbytes">WsPushBytes</a> function to request that data be written.

## -parameters

### -param callbackState [in]

A 
           void pointer to the user-defined state that was passed to <a href="/windows/desktop/api/webservices/nf-webservices-wspushbytes">WsPushBytes</a>.

### -param writeCallback [in]

The
          callback function for writing bytes to the document.

### -param writeCallbackState [in]

A  void  pointer to the caller-defined state that should be passed when invoking the <a href="/windows/desktop/api/webservices/nc-webservices-ws_write_callback">WS_WRITE_CALLBACK</a> function.

### -param asyncContext [in, optional]

A pointer to a <a href="/windows/desktop/api/webservices/ns-webservices-ws_async_context">WS_ASYNC_CONTEXT</a> structure containing information on how to invoke the function asynchronously.  Assign  <b>NULL</b> if invoking synchronously.

### -param error [in, optional]

A  pointer to a <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> data structure where additional error information should be stored if the function fails.

## -returns

This callback function does not return a value.
