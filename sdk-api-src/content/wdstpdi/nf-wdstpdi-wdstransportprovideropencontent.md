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

# WdsTransportProviderOpenContent function


## -description


Opens a new static view of a content stream.


## -parameters




### -param hInstance [in]

Handle to the instance against which this content will be opened. 


### -param pwszContentName [in]

The name of the content stream.


### -param phContent [out]

Pointer to a handle that identifies this content stream to the provider. 




## -returns



If the function succeeds, the return is <b>S_OK</b>.




## -remarks



This callback is required.

When the handle returned by this function is no longer needed it should be closed with using the <a href="https://msdn.microsoft.com/358fdf14-b57b-4c07-b0a5-d8f49aa96c21">WdsTransportProviderCloseContent</a> callback.



