---
UID: NF:strmif.IGraphConfig.RemoveFilterFromCache
title: IGraphConfig::RemoveFilterFromCache (strmif.h)
description: The RemoveFilterFromCache method removes a filter from the filter cache.
helpviewer_keywords: ["IGraphConfig interface [DirectShow]","RemoveFilterFromCache method","IGraphConfig.RemoveFilterFromCache","IGraphConfig::RemoveFilterFromCache","IGraphConfigRemoveFilterFromCache","RemoveFilterFromCache","RemoveFilterFromCache method [DirectShow]","RemoveFilterFromCache method [DirectShow]","IGraphConfig interface","dshow.igraphconfig_removefilterfromcache","strmif/IGraphConfig::RemoveFilterFromCache"]
old-location: dshow\igraphconfig_removefilterfromcache.htm
tech.root: dshow
ms.assetid: a23710d0-85aa-4ae0-84ea-03b9e22091ad
ms.date: 4/26/2023
ms.keywords: IGraphConfig interface [DirectShow],RemoveFilterFromCache method, IGraphConfig.RemoveFilterFromCache, IGraphConfig::RemoveFilterFromCache, IGraphConfigRemoveFilterFromCache, RemoveFilterFromCache, RemoveFilterFromCache method [DirectShow], RemoveFilterFromCache method [DirectShow],IGraphConfig interface, dshow.igraphconfig_removefilterfromcache, strmif/IGraphConfig::RemoveFilterFromCache
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
 - IGraphConfig::RemoveFilterFromCache
 - strmif/IGraphConfig::RemoveFilterFromCache
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
 - IGraphConfig.RemoveFilterFromCache
---

# IGraphConfig::RemoveFilterFromCache


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>RemoveFilterFromCache</code> method removes a filter from the filter cache.

## -parameters

### -param pFilter [in]

Pointer to the <a href="/windows/desktop/api/strmif/nn-strmif-ibasefilter">IBaseFilter</a> interface of the filter to remove from the cache.

## -returns

Returns one of the following <b>HRESULT</b> values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Filter was not in the cache.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Filter was successfully removed from the cache.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-igraphconfig">IGraphConfig Interface</a>