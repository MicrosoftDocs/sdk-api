---
UID: NF:msinkaut.IInkPicture.HitTestSelection
title: IInkPicture::HitTestSelection
author: windows-sdk-content
description: Retrieves a member of the SelectionHitResult enumeration, which specifies which part of a selection, if any, was hit during a hit test.
old-location: tablet\inkpicture_hittestselection.htm
tech.root: tablet
ms.assetid: 8dc745d8-7e2a-4255-86c6-226bf82d3d64
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 8dc745d8-7e2a-4255-86c6-226bf82d3d64, HitTestSelection, HitTestSelection method [Tablet PC], HitTestSelection method [Tablet PC],IInkPicture interface, IInkPicture interface [Tablet PC],HitTestSelection method, IInkPicture.HitTestSelection, IInkPicture::HitTestSelection, msinkaut/IInkPicture::HitTestSelection, tablet.inkpicture_hittestselection
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
 - IInkPicture.HitTestSelection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/en-us/library/Mt846800(v=VS.85).aspx">IInkPicture</a>



<a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a>



<a href="https://msdn.microsoft.com/a93d0121-e271-4656-9cdc-ae05fd19ac8b">SelectionHitResult Enumeration</a>
 

 

