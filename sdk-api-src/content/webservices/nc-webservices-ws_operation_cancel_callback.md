---
UID: NC:webservices.WS_OPERATION_CANCEL_CALLBACK
title: WS_OPERATION_CANCEL_CALLBACK (webservices.h)
description: Gives notification of the cancellation of an asynchronous service operation call as a result of an aborted shutdown of service host.
helpviewer_keywords: ["WS_OPERATION_CANCEL_CALLBACK","WS_OPERATION_CANCEL_CALLBACK callback","WS_OPERATION_CANCEL_CALLBACK callback function [Web Services for Windows]","webservices/WS_OPERATION_CANCEL_CALLBACK","wsw.ws_operation_cancel_callback"]
old-location: wsw\ws_operation_cancel_callback.htm
tech.root: wsw
ms.assetid: 177f9abb-861d-42a9-8044-25076b026f1d
ms.date: 12/05/2018
ms.keywords: WS_OPERATION_CANCEL_CALLBACK, WS_OPERATION_CANCEL_CALLBACK callback, WS_OPERATION_CANCEL_CALLBACK callback function [Web Services for Windows], webservices/WS_OPERATION_CANCEL_CALLBACK, wsw.ws_operation_cancel_callback
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
 - WS_OPERATION_CANCEL_CALLBACK
 - webservices/WS_OPERATION_CANCEL_CALLBACK
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
 - WS_OPERATION_CANCEL_CALLBACK
---

# WS_OPERATION_CANCEL_CALLBACK callback function


## -description

Gives notification of the cancellation of an 
                asynchronous service operation call as a result of an aborted shutdown of service host. 
             This callback is invoked by service model.

## -parameters

### -param reason [in]

Specifies the reason for which the call back is called.

### -param state [in]

A reference to the application defined state registered with the callback.

## -remarks

See <a href="/windows/desktop/api/webservices/nf-webservices-wsregisteroperationforcancel">WsRegisterOperationForCancel</a> for details.
