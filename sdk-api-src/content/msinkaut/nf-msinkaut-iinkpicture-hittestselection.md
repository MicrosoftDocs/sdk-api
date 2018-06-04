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

# IInkPicture::HitTestSelection


## -description



Retrieves a member of the <a href="https://msdn.microsoft.com/a93d0121-e271-4656-9cdc-ae05fd19ac8b">SelectionHitResult</a> enumeration, which specifies which part of a selection, if any, was hit during a hit test.




## -parameters




### -param x [in]

The x-position, in pixels, of the hit test.


### -param y [in]

The y-position, in pixels, of the hit test.


### -param SelArea [out]

The value from the <a href="https://msdn.microsoft.com/a93d0121-e271-4656-9cdc-ae05fd19ac8b">SelectionHitResult</a> enumeration.


## -remarks



For further details about this method, refer to the <a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay</a> object's <a href="https://msdn.microsoft.com/289589fa-84da-40b3-b60e-551ef0114279">HitTestSelection</a> method, which has the same functionality.




## -see-also




<a href="tablet.iinkpicture">IInkPicture</a>



<a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a>



<a href="https://msdn.microsoft.com/a93d0121-e271-4656-9cdc-ae05fd19ac8b">SelectionHitResult Enumeration</a>
 

 

