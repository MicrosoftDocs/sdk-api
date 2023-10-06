---
UID: NF:strmif.IGraphConfig.GetFilterFlags
title: IGraphConfig::GetFilterFlags (strmif.h)
description: The GetFilterFlags method retrieves a filter's configuration information.
helpviewer_keywords: ["GetFilterFlags","GetFilterFlags method [DirectShow]","GetFilterFlags method [DirectShow]","IGraphConfig interface","IGraphConfig interface [DirectShow]","GetFilterFlags method","IGraphConfig.GetFilterFlags","IGraphConfig::GetFilterFlags","IGraphConfigGetFilterFlags","dshow.igraphconfig_getfilterflags","strmif/IGraphConfig::GetFilterFlags"]
old-location: dshow\igraphconfig_getfilterflags.htm
tech.root: dshow
ms.assetid: 747c3865-1969-45e8-a2c9-dbd72a9ea463
ms.date: 4/26/2023
ms.keywords: GetFilterFlags, GetFilterFlags method [DirectShow], GetFilterFlags method [DirectShow],IGraphConfig interface, IGraphConfig interface [DirectShow],GetFilterFlags method, IGraphConfig.GetFilterFlags, IGraphConfig::GetFilterFlags, IGraphConfigGetFilterFlags, dshow.igraphconfig_getfilterflags, strmif/IGraphConfig::GetFilterFlags
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
 - IGraphConfig::GetFilterFlags
 - strmif/IGraphConfig::GetFilterFlags
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
 - IGraphConfig.GetFilterFlags
---

# IGraphConfig::GetFilterFlags


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetFilterFlags</code> method retrieves a filter's configuration information.

## -parameters

### -param pFilter [in]

Pointer to the <a href="/windows/desktop/api/strmif/nn-strmif-ibasefilter">IBaseFilter</a> interface of a filter in the filter graph.

### -param pdwFlags [out]

Receives the current configuration flags.

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
Null pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_IN_GRAPH</b></dt>
</dl>
</td>
<td width="60%">
The filter is not in the graph.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-igraphconfig">IGraphConfig Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-igraphconfig-setfilterflags">IGraphConfig::SetFilterFlags</a>