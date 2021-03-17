---
UID: NS:webservices._WS_ASYNC_CONTEXT
title: WS_ASYNC_CONTEXT (webservices.h)
description: Used with the Async Model to specify the asynchronous callback and a pointer which will be passed to the asynchronous callback.
helpviewer_keywords: ["WS_ASYNC_CONTEXT","WS_ASYNC_CONTEXT structure [Web Services for Windows]","webservices/WS_ASYNC_CONTEXT","wsw.ws_async_context"]
old-location: wsw\ws_async_context.htm
tech.root: wsw
ms.assetid: 3c9ffbef-2f5b-42b0-96b1-f17f0ab98ca4
ms.date: 12/05/2018
ms.keywords: WS_ASYNC_CONTEXT, WS_ASYNC_CONTEXT structure [Web Services for Windows], webservices/WS_ASYNC_CONTEXT, wsw.ws_async_context
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
req.typenames: WS_ASYNC_CONTEXT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_ASYNC_CONTEXT
 - webservices/_WS_ASYNC_CONTEXT
 - WS_ASYNC_CONTEXT
 - webservices/WS_ASYNC_CONTEXT
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
 - WS_ASYNC_CONTEXT
---

# WS_ASYNC_CONTEXT structure


## -description

Used with the Async Model to specify the asynchronous callback and
                a pointer which will be passed to the asynchronous callback.

## -struct-fields

### -field callback

The callback function to call if the operation completes asynchronously.
                    This field may not be <b>NULL</b>.

### -field callbackState

A pointer to user-defined data which will passed to the asynchronous callback
                    function if the operation completes asynchronously.

