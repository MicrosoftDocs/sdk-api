---
UID: NF:rtscom.IDynamicRenderer.put_DataCacheEnabled
title: IDynamicRenderer::put_DataCacheEnabled (rtscom.h)
description: Gets or sets a value that indicates whether data caching is enabled for the DynamicRenderer Class object. (Put)
helpviewer_keywords: ["1b2435ee-4682-4499-aa5c-35201ab2ba95","DataCacheEnabled property [Tablet PC]","DataCacheEnabled property [Tablet PC]","IDynamicRenderer interface","IDynamicRenderer interface [Tablet PC]","DataCacheEnabled property","IDynamicRenderer.DataCacheEnabled","IDynamicRenderer.get_DataCacheEnabled","IDynamicRenderer.put_DataCacheEnabled","IDynamicRenderer::DataCacheEnabled","IDynamicRenderer::get_DataCacheEnabled","IDynamicRenderer::put_DataCacheEnabled","put_DataCacheEnabled","rtscom/IDynamicRenderer::DataCacheEnabled","rtscom/IDynamicRenderer::get_DataCacheEnabled","rtscom/IDynamicRenderer::put_DataCacheEnabled","tablet.idynamicrenderer_datacacheenabled"]
old-location: tablet\idynamicrenderer_datacacheenabled.htm
tech.root: tablet
ms.assetid: 1b2435ee-4682-4499-aa5c-35201ab2ba95
ms.date: 12/05/2018
ms.keywords: 1b2435ee-4682-4499-aa5c-35201ab2ba95, DataCacheEnabled property [Tablet PC], DataCacheEnabled property [Tablet PC],IDynamicRenderer interface, IDynamicRenderer interface [Tablet PC],DataCacheEnabled property, IDynamicRenderer.DataCacheEnabled, IDynamicRenderer.get_DataCacheEnabled, IDynamicRenderer.put_DataCacheEnabled, IDynamicRenderer::DataCacheEnabled, IDynamicRenderer::get_DataCacheEnabled, IDynamicRenderer::put_DataCacheEnabled, put_DataCacheEnabled, rtscom/IDynamicRenderer::DataCacheEnabled, rtscom/IDynamicRenderer::get_DataCacheEnabled, rtscom/IDynamicRenderer::put_DataCacheEnabled, tablet.idynamicrenderer_datacacheenabled
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
 - IDynamicRenderer::put_DataCacheEnabled
 - rtscom/IDynamicRenderer::put_DataCacheEnabled
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
 - IDynamicRenderer.DataCacheEnabled
 - IDynamicRenderer.get_DataCacheEnabled
 - IDynamicRenderer.put_DataCacheEnabled
 - IDynamicRenderer.get_DataCacheEnabled
 - IDynamicRenderer.put_DataCacheEnabled
---

# IDynamicRenderer::put_DataCacheEnabled


## -description

Gets or sets a value that indicates whether data caching is enabled for the <a href="/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)">DynamicRenderer Class</a> object.



This property is read/write.

## -parameters

## -remarks

Setting the <b>DataCacheEnabled</b> property to <b>TRUE</b> enables you to manage the situation where slow processes block the output queue. When the window is invalidated after strokes are drawn by the <a href="/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)">DynamicRenderer Class</a> object, there may be a delay before the collected strokes are drawn. Place the strokes of the dynamic renderer in a cache and use the <a href="/windows/desktop/api/rtscom/nf-rtscom-idynamicrenderer-refresh">IDynamicRenderer::Refresh Method</a> method to redraw the strokes.

After the strokes are collected, you must release them from the cache by calling the <a href="/windows/desktop/api/rtscom/nf-rtscom-idynamicrenderer-releasecacheddata">IDynamicRenderer::ReleaseCachedData Method</a> method. Use the <a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-customstylusdataadded">IStylusPlugin::CustomStylusDataAdded Method</a> method to release the strokes.

It is also useful to set the <b>DataCacheEnabled</b> property to <b>TRUE</b> when you want to display strokes as they are drawn, but have no need to store the strokes after you have done something with them. In this case, store the data identifiers in the data parameter of the <a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-customstylusdataadded">IStylusPlugin::CustomStylusDataAdded Method</a> method, and then release the data when you no longer need the cached strokes.

If this property is <b>TRUE</b>, you must call the <a href="/windows/desktop/api/rtscom/nf-rtscom-idynamicrenderer-releasecacheddata">IDynamicRenderer::ReleaseCachedData Method</a> method for strokes which have been stored in the ink collecting object. If <b>FALSE</b>, you are not required to call the <b>IDynamicRenderer::ReleaseCachedData Method</b> method. The disadvantage to setting this property to <b>FALSE</b> is that any stroke data that was initially dynamically rendered but invalidated by other miscellaneous operations does not render until the stroke data reaches the ink collection object and is rendered there.

Setting this property to <b>FALSE</b> clears the cached data.

## -see-also

<a href="/windows/desktop/api/rtscom/nn-rtscom-idynamicrenderer">IDynamicRenderer Interface</a>



<a href="/windows/desktop/api/rtscom/nf-rtscom-idynamicrenderer-releasecacheddata">IDynamicRenderer::ReleaseCachedData Method</a>
