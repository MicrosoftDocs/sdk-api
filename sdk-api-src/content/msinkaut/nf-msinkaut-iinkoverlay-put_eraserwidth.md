---
UID: NF:msinkaut.IInkOverlay.put_EraserWidth
title: IInkOverlay::put_EraserWidth
author: windows-sdk-content
description: Gets or sets the value that specifies the width of the eraser pen tip.
old-location: tablet\inkoverlay_eraserwidth.htm
old-project: tablet
ms.assetid: d6200640-cf51-44d8-be5a-9dfa5ac36dbc
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: EraserWidth property [Tablet PC], EraserWidth property [Tablet PC],IInkOverlay interface, IInkOverlay interface [Tablet PC],EraserWidth property, IInkOverlay.EraserWidth, IInkOverlay.put_EraserWidth, IInkOverlay::EraserWidth, IInkOverlay::get_EraserWidth, IInkOverlay::put_EraserWidth, InkOverlay.get_EraserWidth, InkOverlay.put_EraserWidth, d6200640-cf51-44d8-be5a-9dfa5ac36dbc, get_EraserWidth, msinkaut/IInkOverlay::EraserWidth, msinkaut/IInkOverlay::get_EraserWidth, msinkaut/IInkOverlay::put_EraserWidth, put_EraserWidth, tablet.inkoverlay_eraserwidth
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
 - IInkOverlay.EraserWidth
 - IInkOverlay.get_EraserWidth
 - IInkOverlay.put_EraserWidth
 - InkOverlay.get_EraserWidth
 - InkOverlay.put_EraserWidth
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkOverlay::put_EraserWidth


## -description



Gets or sets the value that specifies the width of the eraser pen tip.



This property is read/write.


## -parameters


## -remarks



The value specifies the width of the eraser pen tip in ink space units.

You cannot assign negative values to this property.

This property applies only when the <a href="https://msdn.microsoft.com/3b734da3-5784-4504-b22e-b86844d42f4e">EditingMode</a> property is set to <b>IOEM_Delete</b> and the <a href="https://msdn.microsoft.com/87dfd750-254a-4829-b5a2-04aee9890dd0">EraserMode</a> property is set to <b>IOERM_PointErase</b>.




## -see-also




<a href="https://msdn.microsoft.com/3b734da3-5784-4504-b22e-b86844d42f4e">EditingMode Property [InkOverlay Class]</a>



<a href="https://msdn.microsoft.com/87dfd750-254a-4829-b5a2-04aee9890dd0">EraserMode Property [InkOverlay Class]</a>



<a href="tablet.iinkoverlay">IInkOverlay</a>



<a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay Class</a>



<a href="https://msdn.microsoft.com/de25636c-b8ca-47e4-ae16-182b98ede8f6">InkOverlayEditingMode Enumeration</a>



<a href="https://msdn.microsoft.com/e7400a40-9b82-4750-8e92-a39c6f25b7cd">InkOverlayEraserMode Enumeration</a>
 

 

