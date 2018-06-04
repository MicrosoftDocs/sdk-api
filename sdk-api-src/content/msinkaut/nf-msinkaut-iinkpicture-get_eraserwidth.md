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



<a href="tablet.iinkpicture">IInkPicture</a>



<a href="https://msdn.microsoft.com/1ced9779-dae5-4f9a-8a68-b2c0d041d5b4">InkPicture Control</a>
 

 

