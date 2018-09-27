---
UID: NC:webservices.WS_PUSH_BYTES_CALLBACK
title: WS_PUSH_BYTES_CALLBACK
author: windows-sdk-content
description: Used by the WsPushBytes function to request that data be written.
old-location: wsw\ws_push_bytes_callback.htm
tech.root: wsw
ms.assetid: e2f88488-94b7-41c8-95ae-9c409b132466
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: WS_PUSH_BYTES_CALLBACK, WS_PUSH_BYTES_CALLBACK callback, WS_PUSH_BYTES_CALLBACK callback function [Web Services for Windows], webservices/WS_PUSH_BYTES_CALLBACK, wsw.ws_push_bytes_callback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - WebServices.h
api_name:
 - WS_PUSH_BYTES_CALLBACK
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WS_PUSH_BYTES_CALLBACK callback function


## -description


Used by the <a href="https://msdn.microsoft.com/295eb530-00f1-4e80-bd8a-ffb3eb1fad5b">WsPushBytes</a> function to request that data be written.
      


## -parameters




### -param *callbackState [in]

A 
           void pointer to the user-defined state that was passed to <a href="https://msdn.microsoft.com/295eb530-00f1-4e80-bd8a-ffb3eb1fad5b">WsPushBytes</a>.
        


### -param writeCallback [in]

The
          callback function for writing bytes to the document.
        


### -param *writeCallbackState [in]

A  void  pointer to the caller-defined state that should be passed when invoking the <a href="https://msdn.microsoft.com/8d106ac2-226d-4e0c-8f14-8d3e17f15548">WS_WRITE_CALLBACK</a> function.
        


### -param *asyncContext [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/3c9ffbef-2f5b-42b0-96b1-f17f0ab98ca4">WS_ASYNC_CONTEXT</a> structure containing information on how to invoke the function asynchronously.  Assign  <b>NULL</b> if invoking synchronously.


### -param *error [in, optional]

A  pointer to a <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> data structure where additional error information should be stored if the function fails.
        


## -returns



This callback function does not return a value.



