---
UID: NN:strmif.IEnumFilters
title: IEnumFilters (strmif.h)
description: The IEnumFilters interface enumerates the filters in a filter graph.
helpviewer_keywords: ["IEnumFilters","IEnumFilters interface [DirectShow]","IEnumFilters interface [DirectShow]","described","IEnumFiltersInterface","dshow.ienumfilters","strmif/IEnumFilters"]
old-location: dshow\ienumfilters.htm
tech.root: dshow
ms.assetid: e105ccff-86c6-45d5-aead-6d303d038e5a
ms.date: 4/26/2023
ms.keywords: IEnumFilters, IEnumFilters interface [DirectShow], IEnumFilters interface [DirectShow],described, IEnumFiltersInterface, dshow.ienumfilters, strmif/IEnumFilters
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IEnumFilters
 - strmif/IEnumFilters
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
 - IEnumFilters
---

# IEnumFilters interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IEnumFilters</code> interface enumerates the filters in a filter graph. To obtain this interface, call the <a href="/windows/desktop/api/strmif/nf-strmif-ifiltergraph-enumfilters">IFilterGraph::EnumFilters</a> method on the Filter Graph Manager. For more information, see <a href="/windows/desktop/DirectShow/enumerating-objects-in-a-filter-graph">Enumerating Objects in a Filter Graph</a>.

This interface implements a standard Component Object Model (COM) collection object.

If the set of filters in the graph changes, some methods on this interface return VFW_E_ENUM_OUT_OF_SYNC. Call the <a href="/windows/desktop/api/strmif/nf-strmif-ienumfilters-reset">IEnumFilters::Reset</a> method to resynchronize the enumerator.

## -inheritance

The <b>IEnumFilters</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumFilters</b> also has these types of members:

