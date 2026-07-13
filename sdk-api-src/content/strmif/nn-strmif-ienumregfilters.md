---
UID: NN:strmif.IEnumRegFilters
title: IEnumRegFilters (strmif.h)
description: Note  This interface has been deprecated. (IEnumRegFilters)
helpviewer_keywords: ["IEnumRegFilters","IEnumRegFilters interface [DirectShow]","IEnumRegFilters interface [DirectShow]","described","IEnumRegFiltersInterface","dshow.ienumregfilters","strmif/IEnumRegFilters"]
old-location: dshow\ienumregfilters.htm
tech.root: dshow
ms.assetid: 59cb809d-84f5-42c4-a385-0f586af4d048
ms.date: 4/26/2023
ms.keywords: IEnumRegFilters, IEnumRegFilters interface [DirectShow], IEnumRegFilters interface [DirectShow],described, IEnumRegFiltersInterface, dshow.ienumregfilters, strmif/IEnumRegFilters
req.header: strmif.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumRegFilters
 - strmif/IEnumRegFilters
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmif.h
api_name:
 - IEnumRegFilters
---

# IEnumRegFilters interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface has been deprecated. New applications should call <a href="/windows/desktop/api/strmif/nf-strmif-ifiltermapper2-enummatchingfilters">IFilterMapper2::EnumMatchingFilters</a>, which enumerates monikers and returns a pointer to the <b>IEnumMoniker</b> interface.</div>
<div> </div>
This interface provides methods for enumerating registered filters. The <a href="/windows/desktop/api/strmif/nf-strmif-ifiltermapper-enummatchingfilters">IFilterMapper::EnumMatchingFilters</a> method returns a pointer to this interface. However, <a href="/windows/desktop/api/strmif/nn-strmif-ifiltermapper">IFilterMapper</a> has been deprecated in favor of <a href="/windows/desktop/api/strmif/nn-strmif-ifiltermapper2">IFilterMapper2</a>.

## -inheritance

The <b>IEnumRegFilters</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumRegFilters</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/deprecated-interfaces">Deprecated Interfaces</a>
