---
UID: NF:msinkaut.IInkOverlay.put_Selection
title: IInkOverlay::put_Selection
author: windows-sdk-content
description: Gets or sets the InkStrokes collection that is currently selected inside the InkOverlay object or the InkPicture control.
old-location: tablet\inkoverlay_selection.htm
old-project: tablet
ms.assetid: fed95f40-d0c4-43a3-9d15-ce9d4d573b5c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IInkOverlay interface [Tablet PC],Selection property, IInkOverlay.Selection, IInkOverlay.put_Selection, IInkOverlay::Selection, IInkOverlay::get_Selection, IInkOverlay::put_Selection, InkOverlay.get_Selection, InkOverlay.put_Selection, Selection property [Tablet PC], Selection property [Tablet PC],IInkOverlay interface, fed95f40-d0c4-43a3-9d15-ce9d4d573b5c, msinkaut/IInkOverlay::Selection, msinkaut/IInkOverlay::get_Selection, msinkaut/IInkOverlay::put_Selection, put_Selection, tablet.inkoverlay_selection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: TabletPropertyMetricUnit
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkOverlay.Selection
 - IInkOverlay.get_Selection
 - IInkOverlay.put_Selection
 - InkOverlay.get_Selection
 - InkOverlay.put_Selection
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkOverlay::put_Selection


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
 

 

