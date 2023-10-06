---
UID: NF:strmif.IAMOverlayFX.QueryOverlayFXCaps
title: IAMOverlayFX::QueryOverlayFXCaps (strmif.h)
description: The QueryOverlayFXCaps method retrieves information about which overlay effects are available to the Overlay Mixer filter.
helpviewer_keywords: ["IAMOverlayFX interface [DirectShow]","QueryOverlayFXCaps method","IAMOverlayFX.QueryOverlayFXCaps","IAMOverlayFX::QueryOverlayFXCaps","IAMOverlayFXQueryOverlayFXCaps","QueryOverlayFXCaps","QueryOverlayFXCaps method [DirectShow]","QueryOverlayFXCaps method [DirectShow]","IAMOverlayFX interface","dshow.iamoverlayfx_queryoverlayfxcaps","strmif/IAMOverlayFX::QueryOverlayFXCaps"]
old-location: dshow\iamoverlayfx_queryoverlayfxcaps.htm
tech.root: dshow
ms.assetid: 01fdbe3d-bec7-4e66-87c5-b7e6c1044e8a
ms.date: 4/26/2023
ms.keywords: IAMOverlayFX interface [DirectShow],QueryOverlayFXCaps method, IAMOverlayFX.QueryOverlayFXCaps, IAMOverlayFX::QueryOverlayFXCaps, IAMOverlayFXQueryOverlayFXCaps, QueryOverlayFXCaps, QueryOverlayFXCaps method [DirectShow], QueryOverlayFXCaps method [DirectShow],IAMOverlayFX interface, dshow.iamoverlayfx_queryoverlayfxcaps, strmif/IAMOverlayFX::QueryOverlayFXCaps
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
 - IAMOverlayFX::QueryOverlayFXCaps
 - strmif/IAMOverlayFX::QueryOverlayFXCaps
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
 - IAMOverlayFX.QueryOverlayFXCaps
---

# IAMOverlayFX::QueryOverlayFXCaps


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>QueryOverlayFXCaps</code> method retrieves information about which overlay effects are available to the Overlay Mixer filter.

## -parameters

### -param lpdwOverlayFXCaps [out]

Pointer to a variable that receives a value indicating the overlay effects capabilities of the overlay surface. The value is a logical combination of flags from the <a href="/windows/desktop/api/strmif/ne-strmif-amoverlayfx">AMOVERLAYFX</a> enumeration.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface. The DirectShow implementation returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure.

</td>
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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamoverlayfx">IAMOverlayFX Interface</a>