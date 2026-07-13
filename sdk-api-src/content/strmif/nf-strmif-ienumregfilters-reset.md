---
UID: NF:strmif.IEnumRegFilters.Reset
title: IEnumRegFilters::Reset (strmif.h)
description: Note  The IEnumRegFilters interface is deprecated. Resets the enumerator so that the next call to the IEnumRegFilters::Next method begins again at the first filter, if any.
helpviewer_keywords: ["IEnumRegFilters interface [DirectShow]","Reset method","IEnumRegFilters.Reset","IEnumRegFilters::Reset","IEnumRegFiltersReset","Reset","Reset method [DirectShow]","Reset method [DirectShow]","IEnumRegFilters interface","dshow.ienumregfilters_reset","strmif/IEnumRegFilters::Reset"]
old-location: dshow\ienumregfilters_reset.htm
tech.root: dshow
ms.assetid: 095d0102-c845-48ba-a1f5-e0262a924b50
ms.date: 4/26/2023
ms.keywords: IEnumRegFilters interface [DirectShow],Reset method, IEnumRegFilters.Reset, IEnumRegFilters::Reset, IEnumRegFiltersReset, Reset, Reset method [DirectShow], Reset method [DirectShow],IEnumRegFilters interface, dshow.ienumregfilters_reset, strmif/IEnumRegFilters::Reset
req.header: strmif.h
req.include-header: Dshow.h
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
 - IEnumRegFilters::Reset
 - strmif/IEnumRegFilters::Reset
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IEnumRegFilters.Reset
---

# IEnumRegFilters::Reset


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  The <b>IEnumRegFilters</b> interface is deprecated.</div>
<div> </div>
Resets the enumerator so that the next call to the <a href="/windows/desktop/api/strmif/nf-strmif-ienumregfilters-next">IEnumRegFilters::Next</a> method begins again at the first filter, if any.



## -returns

Returns S_OK.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ienumregfilters">IEnumRegFilters Interface</a>
