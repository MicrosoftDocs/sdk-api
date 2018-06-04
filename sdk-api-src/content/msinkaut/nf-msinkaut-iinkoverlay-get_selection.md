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

# IInkOverlay::get_Selection


## -description



Gets or sets the <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection that is currently selected inside the <a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay</a> object or the <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> control.



This property is read/write.


## -parameters


## -remarks



To get the bounding rectangle of the <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection after it has been moved or resized, call the <a href="https://msdn.microsoft.com/3b2c8cfc-05e6-4b53-b709-72291ee78471">GetBoundingBox</a> method of the InkStrokes collection returned by this property.

To get the bounding rectangle of the <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection before it was moved, handle the <a href="https://msdn.microsoft.com/78b5ab11-01c0-4bdb-ae1f-ec55774abdce">InkOverlay</a> or the <a href="https://msdn.microsoft.com/669dc6c2-1620-40f3-b4b5-7ab8967e739a">InkPicture</a> event.

To get the bounding rectangle of the <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection before it was resized, handle the <a href="https://msdn.microsoft.com/606d4bdf-b02e-459f-a4cf-050daac6c309">InkOverlay</a> or the <a href="https://msdn.microsoft.com/4e7f461f-2909-40ab-98d8-b763d489eb62">InkPicture</a> event.




## -see-also




<a href="tablet.iinkoverlay">IInkOverlay</a>



<a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay Class</a>



<a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes Collection</a>



<a href="https://msdn.microsoft.com/669dc6c2-1620-40f3-b4b5-7ab8967e739a">SelectionMoved Event [InkPicture Control]</a>



<a href="https://msdn.microsoft.com/4e7f461f-2909-40ab-98d8-b763d489eb62">SelectionResized Event [InkPicture Control]</a>
 

 

