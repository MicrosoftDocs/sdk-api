---
UID: NF:msinkaut.IInkPicture.get_EraserWidth
title: IInkPicture::get_EraserWidth (msinkaut.h)
author: windows-sdk-content
description: Gets or sets a value that specifies the width of the eraser pen tip.
old-location: tablet\inkpicture_eraserwidth.htm
tech.root: tablet
ms.assetid: 8a880a9a-acd4-4cb1-aea7-4d834ecd9490
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 8a880a9a-acd4-4cb1-aea7-4d834ecd9490, EraserWidth property [Tablet PC], EraserWidth property [Tablet PC],IInkPicture interface, IInkPicture interface [Tablet PC],EraserWidth property, IInkPicture.EraserWidth, IInkPicture.get_EraserWidth, IInkPicture::EraserWidth, IInkPicture::get_EraserWidth, IInkPicture::put_EraserWidth, InkPicture.get_EraserWidth, InkPicture.put_EraserWidth, get_EraserWidth, msinkaut/IInkPicture::EraserWidth, msinkaut/IInkPicture::get_EraserWidth, msinkaut/IInkPicture::put_EraserWidth, put_EraserWidth, tablet.inkpicture_eraserwidth
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
 - IInkPicture.EraserWidth
 - IInkPicture.get_EraserWidth
 - IInkPicture.put_EraserWidth
 - InkPicture.get_EraserWidth
 - InkPicture.put_EraserWidth
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkPicture::get_EraserWidth


## -description



Gets or sets a value that specifies the width of the eraser pen tip.



This property is read/write.


## -parameters


## -remarks



The value specifies the width of the eraser pen tip in ink space units.

You cannot assign negative values to this property.

This property applies only when the <a href="https://msdn.microsoft.com/5767f768-d59c-404e-9098-ab5e0c427c7d">EditingMode</a> property is set to <b>IOEM_Delete</b> and the <a href="https://msdn.microsoft.com/f6471163-8209-4dd0-887c-0edd54ebb50e">EraserMode</a> property is set to <b>IOERM_PointErase</b>.  




## -see-also




<a href="https://msdn.microsoft.com/5767f768-d59c-404e-9098-ab5e0c427c7d">EditingMode [InkPicture Control]</a>



<a href="https://msdn.microsoft.com/f6471163-8209-4dd0-887c-0edd54ebb50e">EraserMode [InkPicture Control]</a>



<a href="https://msdn.microsoft.com/e7400a40-9b82-4750-8e92-a39c6f25b7cd">EraserMode Enumeration</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt846800(v=VS.85).aspx">IInkPicture</a>



<a href="https://msdn.microsoft.com/1ced9779-dae5-4f9a-8a68-b2c0d041d5b4">InkPicture Control</a>
 

 

