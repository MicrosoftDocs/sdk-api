---
UID: NF:strmif.IEnumFilters.Skip
title: IEnumFilters::Skip (strmif.h)
description: The Skip method skips over a specified number of filters.
helpviewer_keywords: ["IEnumFilters interface [DirectShow]","Skip method","IEnumFilters.Skip","IEnumFilters::Skip","IEnumFiltersSkip","Skip","Skip method [DirectShow]","Skip method [DirectShow]","IEnumFilters interface","dshow.ienumfilters_skip","strmif/IEnumFilters::Skip"]
old-location: dshow\ienumfilters_skip.htm
tech.root: dshow
ms.assetid: 594e25b1-03a8-4b6c-965c-f34dae9f3d3b
ms.date: 4/26/2023
ms.keywords: IEnumFilters interface [DirectShow],Skip method, IEnumFilters.Skip, IEnumFilters::Skip, IEnumFiltersSkip, Skip, Skip method [DirectShow], Skip method [DirectShow],IEnumFilters interface, dshow.ienumfilters_skip, strmif/IEnumFilters::Skip
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
 - IEnumFilters::Skip
 - strmif/IEnumFilters::Skip
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
 - IEnumFilters.Skip
---

# IEnumFilters::Skip


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>Skip</code> method skips over a specified number of filters.

## -parameters

### -param cFilters [in]

Number of filters to skip.

## -returns

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>S_FALSE</td>
<td>Skipped past the end of the sequence.</td>
</tr>
<tr>
<td>S_OK</td>
<td>Success.</td>
</tr>
<tr>
<td>VFW_E_ENUM_OUT_OF_SYNC</td>
<td>The graph has changed and is now inconsistent with the enumerator.</td>
</tr>
</table>

## -remarks

If the filter graph changes (for example, the application removes a filter), the enumerator is no longer be consistent with the graph, and the method returns VFW_E_ENUM_OUT_OF_SYNC. Discard any data obtained from previous calls to the enumerator, because it might be invalid. Update the enumerator by calling the <a href="/windows/desktop/api/strmif/nf-strmif-ienumfilters-reset">IEnumFilters::Reset</a> method. You can then call the <code>Skip</code> method safely.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ienumfilters">IEnumFilters Interface</a>