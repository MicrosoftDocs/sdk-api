---
UID: NF:msinkaut.IInkCollector.get_CollectingInk
title: IInkCollector::get_CollectingInk
author: windows-sdk-content
description: Gets a value that specifies whether ink is currently being drawn on an ink collector (InkCollector, InkOverlay, or InkPicture).
old-location: tablet\inkcollector_collectingink.htm
tech.root: tablet
ms.assetid: c0ac36a8-e36e-45a7-b047-14d7f7c8ce14
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: CollectingInk property [Tablet PC], CollectingInk property [Tablet PC],IInkCollector interface, IInkCollector interface [Tablet PC],CollectingInk property, IInkCollector.CollectingInk, IInkCollector.get_CollectingInk, IInkCollector::CollectingInk, IInkCollector::get_CollectingInk, InkCollector.get_CollectingInk, c0ac36a8-e36e-45a7-b047-14d7f7c8ce14, get_CollectingInk, msinkaut/IInkCollector::CollectingInk, msinkaut/IInkCollector::get_CollectingInk, tablet.inkcollector_collectingink
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
 - IInkCollector.CollectingInk
 - IInkCollector.get_CollectingInk
 - get_CollectingInk
 - IInkCollector.get_CollectingInk
 - InkCollector.get_CollectingInk
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkCollector::get_CollectingInk


## -description



Gets a value that specifies whether ink is currently being drawn on an ink collector (<a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a>, <a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay</a>, or <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a>).



This property is read-only.


## -parameters


## -remarks



You can use the <b>CollectingInk</b> property to see if ink is being drawn on an ink collector rather than monitoring the <a href="https://msdn.microsoft.com/eaa89dfe-6141-4205-845b-634321130e26">Stroke</a> event.

<div class="alert"><b>Note</b>  Because ink collection is happening on a different thread than your application code, it is possible that the <b>CollectingInk</b> property can change soon after you have checked it. Thus, your code may be operating under the assumption that the ink collector is not collecting ink, when in fact it is. If this occurs, an error is thrown. To be safe, put such code in a try-catch block.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/4E539E4F-2E7F-44ED-A8D0-650BCAFDFAFB">IInkCollector</a>



<a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector Class</a>
 

 

