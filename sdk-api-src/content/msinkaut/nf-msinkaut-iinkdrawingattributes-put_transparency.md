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

# IInkDrawingAttributes::put_Transparency


## -description



Gets or sets a value that indicates the transparency value of ink.



This property is read/write.


## -parameters


## -remarks



<div class="alert"><b>Note</b>  The transparent rendering effect may be different between dynamic and static rendering. In dynamic rendering the <a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp</a> object is rendered as it is drawn, as it is in the <a href="https://msdn.microsoft.com/1e0e231a-82bc-4d22-9467-4c7b29f4b405">DynamicRendering</a> property, for example. In static rendering, you use the <a href="https://msdn.microsoft.com/18f67080-ed56-43af-b0d6-8af35c2e871b">Draw</a> method of the <a href="https://msdn.microsoft.com/66ec7cab-bfc2-4934-93a4-0ab9cb8c96e7">InkRenderer</a> object to render the <b>IInkStrokeDisp</b> object.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/18f67080-ed56-43af-b0d6-8af35c2e871b">Draw Method [InkRenderer Class]</a>



<a href="https://msdn.microsoft.com/3d8b7892-a120-452a-b83c-474df9be5f52">DrawStroke Method</a>



<a href="https://msdn.microsoft.com/1e0e231a-82bc-4d22-9467-4c7b29f4b405">DynamicRendering Property</a>



<a href="tablet.iinkdrawingattributes">IInkDrawingAttributes</a>



<a href="https://msdn.microsoft.com/10ca7ae5-28dd-42a2-98d9-852d4de5869d">InkDrawingAttributes Class</a>



<a href="https://msdn.microsoft.com/66ec7cab-bfc2-4934-93a4-0ab9cb8c96e7">InkRenderer Class</a>
 

 

