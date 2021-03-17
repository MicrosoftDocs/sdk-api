---
UID: NF:rtscom.IDynamicRenderer.Draw
title: IDynamicRenderer::Draw (rtscom.h)
description: Draws the cached data to the specified device context.
helpviewer_keywords: ["Draw","Draw method [Tablet PC]","Draw method [Tablet PC]","IDynamicRenderer interface","IDynamicRenderer interface [Tablet PC]","Draw method","IDynamicRenderer.Draw","IDynamicRenderer::Draw","d0f05fc7-2b54-40fc-823a-dad0a86174d6","rtscom/IDynamicRenderer::Draw","tablet.idynamicrenderer_draw"]
old-location: tablet\idynamicrenderer_draw.htm
tech.root: tablet
ms.assetid: d0f05fc7-2b54-40fc-823a-dad0a86174d6
ms.date: 12/05/2018
ms.keywords: Draw, Draw method [Tablet PC], Draw method [Tablet PC],IDynamicRenderer interface, IDynamicRenderer interface [Tablet PC],Draw method, IDynamicRenderer.Draw, IDynamicRenderer::Draw, d0f05fc7-2b54-40fc-823a-dad0a86174d6, rtscom/IDynamicRenderer::Draw, tablet.idynamicrenderer_draw
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
 - IDynamicRenderer::Draw
 - rtscom/IDynamicRenderer::Draw
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
 - IDynamicRenderer.Draw
---

# IDynamicRenderer::Draw


## -description

Draws the cached data to the specified device context.

## -parameters

### -param hDC [in]

 The handle of the device context on which to draw.

## -returns

For a description of the return values, see <a href="/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus Classes and Interfaces</a>.

## -remarks

You can use <b>IDynamicRenderer::Draw Method</b> for tasks such as double buffering.

<div class="alert"><b>Note</b>  Drawing cached data cannot be used on Microsoft&lt;entity type="reg"/&gt; Windows&lt;entity type="reg"/&gt; XP Tablet PC Edition 2005 systems.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/rtscom/nn-rtscom-idynamicrenderer">IDynamicRenderer Interface</a>



<a href="/windows/desktop/api/rtscom/nf-rtscom-idynamicrenderer-get_datacacheenabled">IDynamicRenderer::DataCacheEnabled Property</a>



<a href="/windows/desktop/api/rtscom/nf-rtscom-idynamicrenderer-get_drawingattributes">IDynamicRenderer::DrawingAttributes Property</a>



<a href="/windows/desktop/api/rtscom/nf-rtscom-idynamicrenderer-releasecacheddata">IDynamicRenderer::ReleaseCachedData Method</a>