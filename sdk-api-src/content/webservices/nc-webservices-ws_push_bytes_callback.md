---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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



