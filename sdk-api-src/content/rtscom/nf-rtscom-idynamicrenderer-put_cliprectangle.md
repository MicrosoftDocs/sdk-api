---
UID: NF:rtscom.IDynamicRenderer.put_ClipRectangle
title: IDynamicRenderer::put_ClipRectangle
author: windows-sdk-content
description: Gets or sets the clipping rectangle for the DynamicRenderer Class object.
old-location: tablet\idynamicrenderer_cliprectangle.htm
old-project: tablet
ms.assetid: 0d3c6d2e-1675-4335-a283-ea14a818469a
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: 0d3c6d2e-1675-4335-a283-ea14a818469a, ClipRectangle property [Tablet PC], ClipRectangle property [Tablet PC],IDynamicRenderer interface, IDynamicRenderer interface [Tablet PC],ClipRectangle property, IDynamicRenderer.ClipRectangle, IDynamicRenderer.get_ClipRectangle, IDynamicRenderer.put_ClipRectangle, IDynamicRenderer::ClipRectangle, IDynamicRenderer::get_ClipRectangle, IDynamicRenderer::put_ClipRectangle, put_ClipRectangle, rtscom/IDynamicRenderer::ClipRectangle, rtscom/IDynamicRenderer::get_ClipRectangle, rtscom/IDynamicRenderer::put_ClipRectangle, tablet.idynamicrenderer_cliprectangle
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: rtscom.h
req.include-header: 
req.redist: 
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
req.typenames: StylusQueue
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RTSCom.dll
api_name:
 - IDynamicRenderer.ClipRectangle
 - IDynamicRenderer.get_ClipRectangle
 - IDynamicRenderer.put_ClipRectangle
 - IDynamicRenderer.get_ClipRectangle
 - IDynamicRenderer.put_ClipRectangle
product: Windows
targetos: Windows
req.lib: 
req.dll: RTSCom.dll
req.irql: 
req.product: ADAM
---

# IDynamicRenderer::put_ClipRectangle


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
 

 

