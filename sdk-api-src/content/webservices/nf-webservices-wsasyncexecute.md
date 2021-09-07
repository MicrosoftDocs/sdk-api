---
UID: NF:webservices.WsAsyncExecute
title: WsAsyncExecute function (webservices.h)
description: Helper function for implementing an asynchronous operation.
helpviewer_keywords: ["WsAsyncExecute","WsAsyncExecute function [Web Services for Windows]","webservices/WsAsyncExecute","wsw.wsasyncexecute"]
old-location: wsw\wsasyncexecute.htm
tech.root: wsw
ms.assetid: 8705ac1a-62ba-4239-aeb6-b35ac5f0dd18
ms.date: 12/05/2018
ms.keywords: WsAsyncExecute, WsAsyncExecute function [Web Services for Windows], webservices/WsAsyncExecute, wsw.wsasyncexecute
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
 - WsAsyncExecute
 - webservices/WsAsyncExecute
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
 - WsAsyncExecute
---

# WsAsyncExecute function


## -description

Helper function for implementing an <a href="/windows/desktop/wsw/asynchronous-model">asynchronous</a> operation.

## -parameters

### -param asyncState [in]

A pointer to the <a href="/windows/desktop/api/webservices/ns-webservices-ws_async_state">WS_ASYNC_STATE</a> structure used during the asynchronous operation.  This is a state maintenance parameter not intended
                for direct use.  The application must allocate  the <b>WS_ASYNC_STATE</b> structure and ensure that it 
                is kept alive during the entire asynchronous operation.  The <b>WS_ASYNC_STATE</b> structure can be reused after an 
                asynchronous operation has completed.

### -param operation [in, optional]

Represents the initial asynchronous operation to be performed.

### -param callbackModel [in]

Indicates whether the callback is being invoked long or short.
                For more information, see <a href="/windows/desktop/api/webservices/ne-webservices-ws_callback_model">WS_CALLBACK_MODEL</a>

### -param callbackState [in]

A void pointer to a user-defined value that is passed to each <a href="/windows/desktop/api/webservices/nc-webservices-ws_async_function">WS_ASYNC_FUNCTION</a>.

### -param asyncContext [in, optional]

Pointer to information for invoking the function asynchronously. Pass <b>NULL</b> to invoke the function synchronously.

### -param error [in, optional]

Pointer to a <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> structure  that receives additional error information if the function fails.

## -returns

If the function succeeds, it returns NO_ERROR; otherwise, it returns an HRESULT error code.

## -remarks

For an understanding of how WWSAPI handles asynchronous operations, see the <a href="/windows/desktop/wsw/asynchronous-model">Asynchronous Model</a> topic. 

In many cases, an asynchronous operation is composed of other asynchronous operations. Each asynchronous operation may return WS_S_ASYNC indicating the callback will be invoked, or any other success or failure code, in which case the callback will not be invoked. The operation must be prepared to accept a <b>NULL</b> WS_ASYNC_CONTEXT indicating that the caller is requesting the operation to be performed synchronously. It must also ensure that the callback is invoked appropriately. In complex asynchronous operations,  <b>WsAsyncExecute</b> simplifies these details.

<b>WsAsyncExecute</b> operates by invoking a user-defined callback which can initiate an asynchrnous operation and indicate a function to be invoked when the asynchronous operation is complete. This sequence continues until the callback does not set another function to invoke. At this point, the callback specified by the WS_ASYNC_CONTEXT will be invoked if any of the operations completed asynchronously. 



The <a href="/windows/desktop/api/webservices/ns-webservices-ws_async_state">WS_ASYNC_STATE</a> parameter is used by <b>WsAsyncExecute</b> to maintain its state, and is not intended to be initialized, inspected, or used by the caller. The caller however, must allocate the <b>WS_ASYNC_STATE</b> and ensure that it is kept alive during the entire asynchronous operation. The <b>WS_ASYNC_STATE</b> may be reused once the asynchronous operation is complete.

The examples <a href="/windows/desktop/wsw/asyncadd3explicitexample">AsyncAdd3ExplicitExample</a> and <a href="/windows/desktop/wsw/asyncadd3implicitexample">AsyncAdd3ImplicitExample</a> demonstrate implementing
                the same asynchronous function manually using <b>WsAsyncExecute</b>.