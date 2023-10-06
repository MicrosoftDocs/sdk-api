---
UID: NF:strmif.IGraphConfig.RemoveFilterEx
title: IGraphConfig::RemoveFilterEx (strmif.h)
description: The RemoveFilterEx method removes a filter from the filter graph.
helpviewer_keywords: ["IGraphConfig interface [DirectShow]","RemoveFilterEx method","IGraphConfig.RemoveFilterEx","IGraphConfig::RemoveFilterEx","IGraphConfigRemoveFilterEx","RemoveFilterEx","RemoveFilterEx method [DirectShow]","RemoveFilterEx method [DirectShow]","IGraphConfig interface","dshow.igraphconfig_removefilterex","strmif/IGraphConfig::RemoveFilterEx"]
old-location: dshow\igraphconfig_removefilterex.htm
tech.root: dshow
ms.assetid: c3298aa2-4eb2-4e47-9f36-5f2cf541d13e
ms.date: 4/26/2023
ms.keywords: IGraphConfig interface [DirectShow],RemoveFilterEx method, IGraphConfig.RemoveFilterEx, IGraphConfig::RemoveFilterEx, IGraphConfigRemoveFilterEx, RemoveFilterEx, RemoveFilterEx method [DirectShow], RemoveFilterEx method [DirectShow],IGraphConfig interface, dshow.igraphconfig_removefilterex, strmif/IGraphConfig::RemoveFilterEx
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGraphConfig::RemoveFilterEx
 - strmif/IGraphConfig::RemoveFilterEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IGraphConfig.RemoveFilterEx
---

# IGraphConfig::RemoveFilterEx


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>RemoveFilterEx</code> method removes a filter from the filter graph.

## -parameters

### -param pFilter [in]

Pointer to the <a href="/windows/desktop/api/strmif/nn-strmif-ibasefilter">IBaseFilter</a> interface of the filter to remove from the graph.

### -param Flags [in]

Combination of flags from the <a href="/windows/desktop/api/strmif/ne-strmif-_rem_filter_flags">REM_FILTER_FLAGS</a> enumerated type.

## -returns

Returns S_OK if successful, or an <b>HRESULT</b> value indicating the cause of the failure.

## -remarks

This method extends the <a href="/windows/desktop/api/strmif/nf-strmif-ifiltergraph-removefilter">IFilterGraph::RemoveFilter</a> method by accepting a flag that specifies the behavior of the method. This flag enables an application to remove a filter without disconnecting the pins automatically, which improves performance when moving groups of connected filters into a new graph.

By default, this method disconnects the filter before removing it from the graph. Use the REMFILTERF_LEAVECONNECTED flag to leave the filter connected.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-igraphconfig">IGraphConfig Interface</a>