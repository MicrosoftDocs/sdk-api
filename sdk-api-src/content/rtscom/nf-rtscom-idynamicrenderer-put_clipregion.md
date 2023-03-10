---
UID: NF:rtscom.IDynamicRenderer.put_ClipRegion
title: IDynamicRenderer::put_ClipRegion (rtscom.h)
description: Gets or sets the clipping region for the DynamicRenderer Class object. (Put)
helpviewer_keywords: ["ClipRegion property [Tablet PC]","ClipRegion property [Tablet PC]","IDynamicRenderer interface","IDynamicRenderer interface [Tablet PC]","ClipRegion property","IDynamicRenderer.ClipRegion","IDynamicRenderer.get_ClipRegion","IDynamicRenderer.put_ClipRegion","IDynamicRenderer::ClipRegion","IDynamicRenderer::get_ClipRegion","IDynamicRenderer::put_ClipRegion","cf11d03d-8f60-44aa-a296-cc44ddc3930a","put_ClipRegion","rtscom/IDynamicRenderer::ClipRegion","rtscom/IDynamicRenderer::get_ClipRegion","rtscom/IDynamicRenderer::put_ClipRegion","tablet.idynamicrenderer_clipregion"]
old-location: tablet\idynamicrenderer_clipregion.htm
tech.root: tablet
ms.assetid: cf11d03d-8f60-44aa-a296-cc44ddc3930a
ms.date: 12/05/2018
ms.keywords: ClipRegion property [Tablet PC], ClipRegion property [Tablet PC],IDynamicRenderer interface, IDynamicRenderer interface [Tablet PC],ClipRegion property, IDynamicRenderer.ClipRegion, IDynamicRenderer.get_ClipRegion, IDynamicRenderer.put_ClipRegion, IDynamicRenderer::ClipRegion, IDynamicRenderer::get_ClipRegion, IDynamicRenderer::put_ClipRegion, cf11d03d-8f60-44aa-a296-cc44ddc3930a, put_ClipRegion, rtscom/IDynamicRenderer::ClipRegion, rtscom/IDynamicRenderer::get_ClipRegion, rtscom/IDynamicRenderer::put_ClipRegion, tablet.idynamicrenderer_clipregion
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
req.lib: 
req.dll: RTSCom.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDynamicRenderer::put_ClipRegion
 - rtscom/IDynamicRenderer::put_ClipRegion
dev_langs:
 - c++
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
---

# IDynamicRenderer::put_ClipRegion


## -description

Gets or sets the clipping region for the <a href="/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)">DynamicRenderer Class</a> object.



This property is read/write.

## -parameters

## -remarks

Data can be rendered to any defined surface. The collection surface for dynamic rendering may consist of more than one clip rectangle.

<div class="alert"><b>Note</b>  Setting the clipping region does not trigger a redraw.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/rtscom/nn-rtscom-idynamicrenderer">IDynamicRenderer Interface</a>



<a href="/windows/desktop/api/rtscom/nf-rtscom-idynamicrenderer-get_cliprectangle">IDynamicRenderer::ClipRectangle Property</a>
