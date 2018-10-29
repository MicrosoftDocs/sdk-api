---
UID: NF:msinkaut.IInkOverlay.get_CollectingInk
title: IInkOverlay::get_CollectingInk
author: windows-sdk-content
description: Gets a value that specifies whether ink is currently being drawn on an ink collector (InkCollector, InkOverlay, or InkPicture).
old-location: tablet\inkoverlay_collectingink.htm
tech.root: tablet
ms.assetid: fa689979-0c8c-4295-9750-3c2fee9af4d9
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: CollectingInk property [Tablet PC], CollectingInk property [Tablet PC],IInkOverlay interface, IInkOverlay interface [Tablet PC],CollectingInk property, IInkOverlay.CollectingInk, IInkOverlay.get_CollectingInk, IInkOverlay::CollectingInk, IInkOverlay::get_CollectingInk, InkOverlay.get_CollectingInk, get_CollectingInk, msinkaut/IInkOverlay::CollectingInk, msinkaut/IInkOverlay::get_CollectingInk, tablet.inkoverlay_collectingink
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: InkObj.dll
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkOverlay.CollectingInk
 - IInkOverlay.get_CollectingInk
 - InkOverlay.get_CollectingInk
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkOverlay::get_CollectingInk


## -description



Gets a value that specifies whether ink is currently being drawn on an ink collector (<a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a>, <a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay</a>, or <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a>).



This property is read-only.


## -parameters


## -remarks



You can use the <a href="https://msdn.microsoft.com/c0ac36a8-e36e-45a7-b047-14d7f7c8ce14">CollectingInk</a> property to see if ink is being drawn on an ink collector rather than monitoring the <a href="https://msdn.microsoft.com/eaa89dfe-6141-4205-845b-634321130e26">Stroke</a> event.

<div class="alert"><b>Note</b>  Because ink collection is happening on a different thread than your application code, it is possible that the <a href="https://msdn.microsoft.com/c0ac36a8-e36e-45a7-b047-14d7f7c8ce14">CollectingInk</a> property can change soon after you have checked it. Thus, your code may be operating under the assumption that the ink collector is not collecting ink, when in fact it is. If this occurs, an error is thrown. To be safe, put such code in a try-catch block.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/ACE11946-113B-42EE-A3F1-0036B1DF8141">IInkOverlay</a>



<a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay Class</a>
 

 

