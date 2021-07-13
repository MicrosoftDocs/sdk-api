---
UID: NF:rtscom.IDynamicRenderer.Refresh
title: IDynamicRenderer::Refresh (rtscom.h)
description: Causes the DynamicRenderer Class object to redraw the ink data that is currently rendering.
helpviewer_keywords: ["409d4353-fc85-49ff-99a4-d8393a3c0ec4","IDynamicRenderer interface [Tablet PC]","Refresh method","IDynamicRenderer.Refresh","IDynamicRenderer::Refresh","Refresh","Refresh method [Tablet PC]","Refresh method [Tablet PC]","IDynamicRenderer interface","rtscom/IDynamicRenderer::Refresh","tablet.idynamicrenderer_refresh"]
old-location: tablet\idynamicrenderer_refresh.htm
tech.root: tablet
ms.assetid: 409d4353-fc85-49ff-99a4-d8393a3c0ec4
ms.date: 12/05/2018
ms.keywords: 409d4353-fc85-49ff-99a4-d8393a3c0ec4, IDynamicRenderer interface [Tablet PC],Refresh method, IDynamicRenderer.Refresh, IDynamicRenderer::Refresh, Refresh, Refresh method [Tablet PC], Refresh method [Tablet PC],IDynamicRenderer interface, rtscom/IDynamicRenderer::Refresh, tablet.idynamicrenderer_refresh
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
 - IDynamicRenderer::Refresh
 - rtscom/IDynamicRenderer::Refresh
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
 - IDynamicRenderer.Refresh
---

# IDynamicRenderer::Refresh


## -description

Causes the <a href="/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)">DynamicRenderer Class</a> object to redraw the ink data that is currently rendering.



## -returns

This method can return one of these values.

## -remarks

If the <a href="/windows/desktop/api/rtscom/nf-rtscom-idynamicrenderer-get_datacacheenabled">IDynamicRenderer::DataCacheEnabled Property</a> property is <b>true</b>, then the <a href="/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)">DynamicRenderer Class</a> object redraws all tablet stylus data not yet released from the cache. If the <b>IDynamicRenderer::DataCacheEnabled Property</b> property is <b>false</b>, then the <b>DynamicRenderer Class</b> object redraws only the current stroke.

When calling the <b>IDynamicRenderer::Refresh Method</b> from within a Paint event handler, set the <a href="/windows/desktop/api/rtscom/nf-rtscom-idynamicrenderer-get_cliprectangle">IDynamicRenderer::ClipRectangle Property</a> to the Paint event's rectangle.

## -see-also

<a href="/windows/desktop/api/rtscom/nf-rtscom-idynamicrenderer-draw">Draw Method</a>



<a href="/windows/desktop/api/rtscom/nn-rtscom-idynamicrenderer">IDynamicRenderer Interface</a>



<a href="/windows/desktop/api/rtscom/nf-rtscom-idynamicrenderer-get_drawingattributes">IDynamicRenderer::DrawingAttributes Property</a>
