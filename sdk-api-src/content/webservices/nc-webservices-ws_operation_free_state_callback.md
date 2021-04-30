---
UID: NC:webservices.WS_OPERATION_FREE_STATE_CALLBACK
title: WS_OPERATION_FREE_STATE_CALLBACK (webservices.h)
description: Allows an application to cleanup state information that was registered with cancellation callback.
helpviewer_keywords: ["WS_OPERATION_FREE_STATE_CALLBACK","WS_OPERATION_FREE_STATE_CALLBACK callback","WS_OPERATION_FREE_STATE_CALLBACK callback function [Web Services for Windows]","webservices/WS_OPERATION_FREE_STATE_CALLBACK","wsw.ws_operation_free_state_callback"]
old-location: wsw\ws_operation_free_state_callback.htm
tech.root: wsw
ms.assetid: 46b30bb3-00c6-4f54-b040-683cd6dd5525
ms.date: 12/05/2018
ms.keywords: WS_OPERATION_FREE_STATE_CALLBACK, WS_OPERATION_FREE_STATE_CALLBACK callback, WS_OPERATION_FREE_STATE_CALLBACK callback function [Web Services for Windows], webservices/WS_OPERATION_FREE_STATE_CALLBACK, wsw.ws_operation_free_state_callback
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
 - WS_OPERATION_FREE_STATE_CALLBACK
 - webservices/WS_OPERATION_FREE_STATE_CALLBACK
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
 - WS_OPERATION_FREE_STATE_CALLBACK
---

# WS_OPERATION_FREE_STATE_CALLBACK callback function


## -description

Allows an application to cleanup state information that was registered with cancellation callback. 
             
This callback is invoked by service model.

## -parameters

### -param state [in]

A reference to the application defined state registered with the callback.

## -remarks

See <a href="/windows/desktop/api/webservices/nf-webservices-wsregisteroperationforcancel">WsRegisterOperationForCancel</a> for details.
