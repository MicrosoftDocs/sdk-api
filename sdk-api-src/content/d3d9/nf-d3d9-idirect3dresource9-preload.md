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

# IDirect3DResource9::PreLoad


## -description


Preloads a managed resource.


## -parameters






## -returns



This method does not return a value.




## -remarks



Calling this method indicates that the application will need this managed resource shortly. This method has no effect on nonmanaged resources.

<b>IDirect3DResource9::PreLoad</b> detects "thrashing" conditions where more resources are being used in each frame than can fit in video memory simultaneously. Under such circumstances <b>IDirect3DResource9::PreLoad</b> silently does nothing.




## -see-also




<a href="https://msdn.microsoft.com/1fdb0bfe-6e36-49ca-b119-a2b3266037d2">IDirect3DResource9</a>
 

 

