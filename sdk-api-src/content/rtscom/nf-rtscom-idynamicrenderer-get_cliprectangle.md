---
UID: NF:rtscom.IDynamicRenderer.get_ClipRectangle
title: IDynamicRenderer::get_ClipRectangle (rtscom.h)
description: Gets or sets the clipping rectangle for the DynamicRenderer Class object. (Get)
helpviewer_keywords: ["0d3c6d2e-1675-4335-a283-ea14a818469a","ClipRectangle property [Tablet PC]","ClipRectangle property [Tablet PC]","IDynamicRenderer interface","IDynamicRenderer interface [Tablet PC]","ClipRectangle property","IDynamicRenderer.ClipRectangle","IDynamicRenderer.get_ClipRectangle","IDynamicRenderer.put_ClipRectangle","IDynamicRenderer::ClipRectangle","IDynamicRenderer::get_ClipRectangle","IDynamicRenderer::put_ClipRectangle","get_ClipRectangle","rtscom/IDynamicRenderer::ClipRectangle","rtscom/IDynamicRenderer::get_ClipRectangle","rtscom/IDynamicRenderer::put_ClipRectangle","tablet.idynamicrenderer_cliprectangle"]
old-location: tablet\idynamicrenderer_cliprectangle.htm
tech.root: tablet
ms.assetid: 0d3c6d2e-1675-4335-a283-ea14a818469a
ms.date: 12/05/2018
ms.keywords: 0d3c6d2e-1675-4335-a283-ea14a818469a, ClipRectangle property [Tablet PC], ClipRectangle property [Tablet PC],IDynamicRenderer interface, IDynamicRenderer interface [Tablet PC],ClipRectangle property, IDynamicRenderer.ClipRectangle, IDynamicRenderer.get_ClipRectangle, IDynamicRenderer.put_ClipRectangle, IDynamicRenderer::ClipRectangle, IDynamicRenderer::get_ClipRectangle, IDynamicRenderer::put_ClipRectangle, get_ClipRectangle, rtscom/IDynamicRenderer::ClipRectangle, rtscom/IDynamicRenderer::get_ClipRectangle, rtscom/IDynamicRenderer::put_ClipRectangle, tablet.idynamicrenderer_cliprectangle
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
 - IDynamicRenderer::get_ClipRectangle
 - rtscom/IDynamicRenderer::get_ClipRectangle
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
 - IDynamicRenderer.ClipRectangle
 - IDynamicRenderer.get_ClipRectangle
 - IDynamicRenderer.put_ClipRectangle
 - IDynamicRenderer.get_ClipRectangle
 - IDynamicRenderer.put_ClipRectangle
---

# IDynamicRenderer::get_ClipRectangle


## -description

Gets or sets the clipping rectangle for the <a href="/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)">DynamicRenderer Class</a> object.



This property is read/write.

## -parameters

## -remarks

The <b>ClipRectangle</b> property is set immediately and applies to the stroke that is being drawn. It differs from the <a href="/windows/desktop/api/rtscom/nf-rtscom-idynamicrenderer-get_drawingattributes">IDynamicRenderer::DrawingAttributes Property</a> property, which applies to the next stroke drawn. This allows the clip rectangle to grow as the stroke is drawn.

When calling the <a href="/windows/desktop/api/rtscom/nf-rtscom-idynamicrenderer-refresh">IDynamicRenderer::Refresh Method</a> from within a Paint event handler, set the <b>IDynamicRenderer::ClipRectangle Property</b> to the Paint event's rectangle.

<div class="alert"><b>Note</b>  If the <b>ClipRectangle</b> is expanded in mid-stroke, then a <a href="/windows/desktop/api/rtscom/nf-rtscom-idynamicrenderer-refresh">IDynamicRenderer::Refresh Method</a> call is required in order to display the new ink. This refresh call must be made every time new ink appears in a new area; however, doing so may cause performance problems when inking in the new area.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)">DynamicRenderer Class</a>



<a href="/windows/desktop/api/rtscom/nn-rtscom-idynamicrenderer">IDynamicRenderer Interface</a>



<a href="/windows/desktop/api/rtscom/nf-rtscom-idynamicrenderer-get_clipregion">IDynamicRenderer::ClipRegion Property</a>
