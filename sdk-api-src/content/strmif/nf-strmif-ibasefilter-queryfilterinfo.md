---
UID: NF:strmif.IBaseFilter.QueryFilterInfo
title: IBaseFilter::QueryFilterInfo (strmif.h)
description: The QueryFilterInfo method retrieves information about the filter.
helpviewer_keywords: ["IBaseFilter interface [DirectShow]","QueryFilterInfo method","IBaseFilter.QueryFilterInfo","IBaseFilter::QueryFilterInfo","IBaseFilterQueryFilterInfo","QueryFilterInfo","QueryFilterInfo method [DirectShow]","QueryFilterInfo method [DirectShow]","IBaseFilter interface","dshow.ibasefilter_queryfilterinfo","strmif/IBaseFilter::QueryFilterInfo"]
old-location: dshow\ibasefilter_queryfilterinfo.htm
tech.root: dshow
ms.assetid: 6cb9b6ef-05ae-4816-b337-dd90cab843fb
ms.date: 4/26/2023
ms.keywords: IBaseFilter interface [DirectShow],QueryFilterInfo method, IBaseFilter.QueryFilterInfo, IBaseFilter::QueryFilterInfo, IBaseFilterQueryFilterInfo, QueryFilterInfo, QueryFilterInfo method [DirectShow], QueryFilterInfo method [DirectShow],IBaseFilter interface, dshow.ibasefilter_queryfilterinfo, strmif/IBaseFilter::QueryFilterInfo
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
 - IBaseFilter::QueryFilterInfo
 - strmif/IBaseFilter::QueryFilterInfo
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
 - IBaseFilter.QueryFilterInfo
---

# IBaseFilter::QueryFilterInfo


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>QueryFilterInfo</code> method retrieves information about the filter.

## -parameters

### -param pInfo [out]

Pointer to a [FILTER_INFO](/windows/desktop/api/strmif/ns-strmif-filter_info) structure.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument

</td>
</tr>
</table>

## -remarks

This method fills the <b>FILTER_INFO</b> structure with the filter information. On return, if the <b>pGraph</b> member of the <b>FILTER_INFO</b> structure is non-<b>NULL</b>, the <a href="/windows/desktop/api/strmif/nn-strmif-ifiltergraph">IFilterGraph</a> interface has an outstanding reference count. Be sure to release the interface when you are done.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ibasefilter">IBaseFilter Interface</a>