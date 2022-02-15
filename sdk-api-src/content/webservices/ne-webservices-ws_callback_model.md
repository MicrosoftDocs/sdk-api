---
UID: NE:webservices.__unnamed_enum_14
title: WS_CALLBACK_MODEL (webservices.h)
description: Specifies the threading behavior of a callback (for example, a WS_ASYNC_CALLBACK).
helpviewer_keywords: ["WS_CALLBACK_MODEL","WS_CALLBACK_MODEL enumeration [Web Services for Windows]","WS_LONG_CALLBACK","WS_SHORT_CALLBACK","webservices/WS_CALLBACK_MODEL","webservices/WS_LONG_CALLBACK","webservices/WS_SHORT_CALLBACK","wsw.ws_callback_model"]
old-location: wsw\ws_callback_model.htm
tech.root: wsw
ms.assetid: 6a8e4c0b-3c0a-4bd3-bbac-40e6f499a055
ms.date: 12/05/2018
ms.keywords: WS_CALLBACK_MODEL, WS_CALLBACK_MODEL enumeration [Web Services for Windows], WS_LONG_CALLBACK, WS_SHORT_CALLBACK, webservices/WS_CALLBACK_MODEL, webservices/WS_LONG_CALLBACK, webservices/WS_SHORT_CALLBACK, wsw.ws_callback_model
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
req.typenames: WS_CALLBACK_MODEL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_CALLBACK_MODEL
 - webservices/WS_CALLBACK_MODEL
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
 - WS_CALLBACK_MODEL
---

# WS_CALLBACK_MODEL enumeration


## -description

Specifies the threading behavior of a callback (for example, a <a href="/windows/desktop/api/webservices/nc-webservices-ws_async_callback">WS_ASYNC_CALLBACK</a>).

## -enum-fields

### -field WS_SHORT_CALLBACK:0

This value is used to indicate that a callback is invoked short.
                

When a callback is invoked short, it should avoid lengthy computation or lengthy
                    blocking calls so that it can return to the caller quickly.  During the time
                    that a callback is executing short, other work items may not be able to be
                    dequeued within the process.  This can lead to starvation deadlock, an
                    unresponsive system, or an underutilized system.
                

If it is necessary to do IO within a callback that was invoked short, the best practice is
                    to use asynchronous IO (instead of synchronous IO), to avoid lengthy blocking calls.

### -field WS_LONG_CALLBACK:1

This value is used to indicate that a callback is invoked long.
                

A callback invoked long is not required to return to the caller quickly.
                

However, long callbacks are a limited resource, so it is not always possible
                    to invoke a callback long.
                

Before invoking a callback long, the caller must ensure that there is another thread
                    available to dequeue work as necessary.  For example, if a caller needs to create 
                    a thread but is unable to, then it must invoke the callback short.
                

All callbacks must be able to deal with being invoked short as well as long:
                    <ul>
<li>A callback that is invoked short but requires long can interpret this as an
                        error condition, likely due to low resources.  For example, calling CreateThread or
                        QueueUserWorkItem in this situation is also likely to fail.  If a
                        callback is required to run long in a low resource situation, then a thread
                        for this purpose must be reserved prior to initiating the async operation.
                        </li>
<li>A callback that is invoked long but expects short can go about its work normally.
                    </li>
</ul>

## -remarks

Whether a callback will be invoked long or short is up to the caller implementation.
                The channel and listener implementations provide a way to control this for async callbacks
                via the <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_property_id">WS_CHANNEL_PROPERTY_ASYNC_CALLBACK_MODEL</a> and 
                <a href="/windows/desktop/api/webservices/ne-webservices-ws_listener_property_id">WS_LISTENER_PROPERTY_ASYNC_CALLBACK_MODEL</a> properties.
