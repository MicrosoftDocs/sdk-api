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

# IDynamicRenderer::get_ClipRectangle


## -description



Gets or sets the clipping rectangle for the <a href="https://msdn.microsoft.com/938e1eb2-3dd4-4e21-9c46-9ef840172b05">DynamicRenderer Class</a> object.



This property is read/write.


## -parameters


## -remarks



The <b>ClipRectangle</b> property is set immediately and applies to the stroke that is being drawn. It differs from the <a href="https://msdn.microsoft.com/d67a85e7-6dfc-4444-bb69-a46e1234d021">IDynamicRenderer::DrawingAttributes Property</a> property, which applies to the next stroke drawn. This allows the clip rectangle to grow as the stroke is drawn.

When calling the <a href="https://msdn.microsoft.com/409d4353-fc85-49ff-99a4-d8393a3c0ec4">IDynamicRenderer::Refresh Method</a> from within a Paint event handler, set the <b>IDynamicRenderer::ClipRectangle Property</b> to the Paint event's rectangle.

<div class="alert"><b>Note</b>  If the <b>ClipRectangle</b> is expanded in mid-stroke, then a <a href="https://msdn.microsoft.com/409d4353-fc85-49ff-99a4-d8393a3c0ec4">IDynamicRenderer::Refresh Method</a> call is required in order to display the new ink. This refresh call must be made every time new ink appears in a new area; however, doing so may cause performance problems when inking in the new area.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/938e1eb2-3dd4-4e21-9c46-9ef840172b05">DynamicRenderer Class</a>



<a href="https://msdn.microsoft.com/6435b297-d6a7-418b-afc0-f8cc0b329842">IDynamicRenderer Interface</a>



<a href="https://msdn.microsoft.com/cf11d03d-8f60-44aa-a296-cc44ddc3930a">IDynamicRenderer::ClipRegion Property</a>
 

 

