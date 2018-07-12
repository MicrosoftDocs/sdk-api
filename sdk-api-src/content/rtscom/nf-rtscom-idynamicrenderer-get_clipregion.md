---
UID: NF:rtscom.IDynamicRenderer.get_ClipRegion
title: IDynamicRenderer::get_ClipRegion
author: windows-sdk-content
description: Gets or sets the clipping region for the DynamicRenderer Class object.
old-location: tablet\idynamicrenderer_clipregion.htm
old-project: tablet
ms.assetid: cf11d03d-8f60-44aa-a296-cc44ddc3930a
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: ClipRegion property [Tablet PC], ClipRegion property [Tablet PC],IDynamicRenderer interface, IDynamicRenderer interface [Tablet PC],ClipRegion property, IDynamicRenderer.ClipRegion, IDynamicRenderer.get_ClipRegion, IDynamicRenderer.put_ClipRegion, IDynamicRenderer::ClipRegion, IDynamicRenderer::get_ClipRegion, IDynamicRenderer::put_ClipRegion, cf11d03d-8f60-44aa-a296-cc44ddc3930a, get_ClipRegion, rtscom/IDynamicRenderer::ClipRegion, rtscom/IDynamicRenderer::get_ClipRegion, rtscom/IDynamicRenderer::put_ClipRegion, tablet.idynamicrenderer_clipregion
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: rtscom.h
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
req.typenames: StylusQueue
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RTSCom.dll
api_name:
 - IDynamicRenderer.ClipRegion
 - IDynamicRenderer.get_ClipRegion
 - IDynamicRenderer.put_ClipRegion
 - IDynamicRenderer.get_ClipRegion
 - IDynamicRenderer.put_ClipRegion
product: Windows
targetos: Windows
req.lib: 
req.dll: RTSCom.dll
req.irql: 
req.product: ADAM
---

# IDynamicRenderer::get_ClipRegion


## -description



Gets or sets the clipping region for the <a href="https://msdn.microsoft.com/938e1eb2-3dd4-4e21-9c46-9ef840172b05">DynamicRenderer Class</a> object.



This property is read/write.


## -parameters


## -remarks



Data can be rendered to any defined surface. The collection surface for dynamic rendering may consist of more than one clip rectangle.

<div class="alert"><b>Note</b>  Setting the clipping region does not trigger a redraw.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/6435b297-d6a7-418b-afc0-f8cc0b329842">IDynamicRenderer Interface</a>



<a href="https://msdn.microsoft.com/0d3c6d2e-1675-4335-a283-ea14a818469a">IDynamicRenderer::ClipRectangle Property</a>
 

 

