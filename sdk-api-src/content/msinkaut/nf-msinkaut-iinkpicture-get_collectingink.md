---
UID: NF:msinkaut.IInkPicture.get_CollectingInk
title: IInkPicture::get_CollectingInk
author: windows-sdk-content
description: Gets a value that specifies whether ink is currently being drawn on an ink collector (InkCollector, InkOverlay, or InkPicture).
old-location: tablet\inkpicture_collectingink.htm
old-project: tablet
ms.assetid: 19fbe26e-02a4-4d05-a2e8-25d2f8ae1146
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CollectingInk property [Tablet PC], CollectingInk property [Tablet PC],IInkPicture interface, IInkPicture interface [Tablet PC],CollectingInk property, IInkPicture.CollectingInk, IInkPicture.get_CollectingInk, IInkPicture::CollectingInk, IInkPicture::get_CollectingInk, InkPicture.get_CollectingInk, get_CollectingInk, msinkaut/IInkPicture::CollectingInk, msinkaut/IInkPicture::get_CollectingInk, tablet.inkpicture_collectingink
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
 - IInkPicture.CollectingInk
 - IInkPicture.get_CollectingInk
 - InkPicture.get_CollectingInk
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkPicture::get_CollectingInk


## -description



Gets a value that specifies whether ink is currently being drawn on an ink collector (<a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a>, <a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay</a>, or <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a>).



This property is read-only.


## -parameters


## -remarks



You can use the <b>CollectingInk</b> property to see if ink is being drawn on an ink collector rather than monitoring the <a href="https://msdn.microsoft.com/2829b65a-6120-402e-91e3-5587d1f456f9">Stroke</a> event.

<div class="alert"><b>Note</b>  Because ink collection is happening on a different thread than your application code, it is possible that the <b>CollectingInk</b> property can change soon after you have checked it. Thus, your code may be operating under the assumption that the ink collector is not collecting ink, when in fact it is. If this occurs, an error is thrown. To be safe, put such code in a try-catch block.</div>
<div> </div>



## -see-also




<a href="tablet.iinkpicture">IInkPicture</a>



<a href="https://msdn.microsoft.com/1ced9779-dae5-4f9a-8a68-b2c0d041d5b4">InkPicture Control</a>
 

 

