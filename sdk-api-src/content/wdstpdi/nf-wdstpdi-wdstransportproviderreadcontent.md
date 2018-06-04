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

# WdsTransportProviderReadContent function


## -description


Reads content from an open content stream. 


## -parameters




### -param hContent [in]

Handle to an open content stream to be read. This is the handle return by the <a href="https://msdn.microsoft.com/95bea971-9c97-4d66-871d-5ef7407b9659">WdsTransportProviderOpenContent</a> callback.


### -param pBuffer [in]

Pointer to location to receive read content.


### -param ulBytesToRead [in]

The size in bytes of the buffer at the location specified by the <i>pBuffer</i> parameter.


### -param pContentOffset [in]

The offset into the content stream specified by <i>hContent</i> from which to start reading.


### -param pvUserData [in]

User specified data passed to the callback function.  


## -returns



If the function succeeds, the return is <b>S_OK</b>.




## -remarks



This callback is required.



