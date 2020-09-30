---
UID: NF:rtscom.IDynamicRenderer.ReleaseCachedData
title: IDynamicRenderer::ReleaseCachedData (rtscom.h)
description: Releases specified stroke data from the temporal data held by DynamicRenderer Class.
helpviewer_keywords: ["691de815-a5be-4982-a59a-b904c070ede8","IDynamicRenderer interface [Tablet PC]","ReleaseCachedData method","IDynamicRenderer.ReleaseCachedData","IDynamicRenderer::ReleaseCachedData","ReleaseCachedData","ReleaseCachedData method [Tablet PC]","ReleaseCachedData method [Tablet PC]","IDynamicRenderer interface","rtscom/IDynamicRenderer::ReleaseCachedData","tablet.idynamicrenderer_releasecacheddata"]
old-location: tablet\idynamicrenderer_releasecacheddata.htm
tech.root: tablet
ms.assetid: 691de815-a5be-4982-a59a-b904c070ede8
ms.date: 12/05/2018
ms.keywords: 691de815-a5be-4982-a59a-b904c070ede8, IDynamicRenderer interface [Tablet PC],ReleaseCachedData method, IDynamicRenderer.ReleaseCachedData, IDynamicRenderer::ReleaseCachedData, ReleaseCachedData, ReleaseCachedData method [Tablet PC], ReleaseCachedData method [Tablet PC],IDynamicRenderer interface, rtscom/IDynamicRenderer::ReleaseCachedData, tablet.idynamicrenderer_releasecacheddata
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
 - IDynamicRenderer::ReleaseCachedData
 - rtscom/IDynamicRenderer::ReleaseCachedData
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
 - IDynamicRenderer.ReleaseCachedData
---

# IDynamicRenderer::ReleaseCachedData


## -description

Releases specified stroke data from the temporal data held by <a href="/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)">DynamicRenderer Class</a>.

## -parameters

### -param strokeId

The identifier for the stroke.

## -returns

For a description of the return values, see <a href="/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus Classes and Interfaces</a>.

## -remarks

This method is used only when the <a href="/windows/desktop/api/rtscom/nf-rtscom-idynamicrenderer-get_datacacheenabled">IDynamicRenderer::DataCacheEnabled Property</a> property is set to <b>true</b>.

The <b>IDynamicRenderer::ReleaseCachedData Method</b> method enables you to release the specified stroke data from the temporal data held by the <a href="/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)">DynamicRenderer Class</a> object.


<a href="/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)">DynamicRenderer Class</a> strokes can be placed in a cache, so they can be redrawn by calling the <a href="/windows/desktop/api/rtscom/nf-rtscom-idynamicrenderer-refresh">IDynamicRenderer::Refresh Method</a> method. After the strokes are collected, release them from the cache by calling the <b>IDynamicRenderer::ReleaseCachedData Method</b> method. Generally, the release occurs in the <a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-customstylusdataadded">IStylusPlugin::CustomStylusDataAdded Method</a> method.

<i>strokeId</i> cannot accept a value of less than zero.

## -see-also

<a href="/windows/desktop/api/rtscom/nf-rtscom-idynamicrenderer-draw">Draw Method</a>



<a href="/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)">DynamicRenderer Class</a>



<a href="/windows/desktop/api/rtscom/nn-rtscom-idynamicrenderer">IDynamicRenderer Interface</a>