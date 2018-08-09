---
UID: NS:webservices._WS_ASYNC_CONTEXT
title: "_WS_ASYNC_CONTEXT"
author: windows-sdk-content
description: Used with the Async Model to specify the asynchronous callback and a pointer which will be passed to the asynchronous callback.
old-location: wsw\ws_async_context.htm
old-project: wsw
ms.assetid: 3c9ffbef-2f5b-42b0-96b1-f17f0ab98ca4
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WS_ASYNC_CONTEXT, WS_ASYNC_CONTEXT structure [Web Services for Windows], _WS_ASYNC_CONTEXT, webservices/WS_ASYNC_CONTEXT, wsw.ws_async_context
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: WS_ASYNC_CONTEXT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_ASYNC_CONTEXT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WS_ASYNC_CONTEXT structure


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
                

