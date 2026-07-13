---
UID: NF:strmif.IPin.ConnectionMediaType
title: IPin::ConnectionMediaType (strmif.h)
description: The ConnectionMediaType method retrieves the media type for the current pin connection, if any.
helpviewer_keywords: ["ConnectionMediaType","ConnectionMediaType method [DirectShow]","ConnectionMediaType method [DirectShow]","IPin interface","IPin interface [DirectShow]","ConnectionMediaType method","IPin.ConnectionMediaType","IPin::ConnectionMediaType","IPinConnectionMediaType","dshow.ipin_connectionmediatype","strmif/IPin::ConnectionMediaType"]
old-location: dshow\ipin_connectionmediatype.htm
tech.root: dshow
ms.assetid: f372bfa7-b0ba-43f9-ba86-cbca5d1de515
ms.date: 4/26/2023
ms.keywords: ConnectionMediaType, ConnectionMediaType method [DirectShow], ConnectionMediaType method [DirectShow],IPin interface, IPin interface [DirectShow],ConnectionMediaType method, IPin.ConnectionMediaType, IPin::ConnectionMediaType, IPinConnectionMediaType, dshow.ipin_connectionmediatype, strmif/IPin::ConnectionMediaType
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
 - IPin::ConnectionMediaType
 - strmif/IPin::ConnectionMediaType
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
 - IPin.ConnectionMediaType
---

# IPin::ConnectionMediaType


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>ConnectionMediaType</code> method retrieves the media type for the current pin connection, if any.

## -parameters

### -param pmt [out]

Pointer to an <a href="/windows/desktop/api/strmif/ns-strmif-am_media_type">AM_MEDIA_TYPE</a> structure that receives the media type.

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
Success.

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
<dt><b>VFW_E_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
Pin is not connected.

</td>
</tr>
</table>

## -remarks

If the pin is connected, this method copies the media type into the <a href="/windows/desktop/api/strmif/ns-strmif-am_media_type">AM_MEDIA_TYPE</a> structure specified by <i>pmt</i>. The caller must free the media type's format block. You can use the Microsoft® Win32®<b>CoTaskMemFree</b> function, or the <a href="/windows/desktop/DirectShow/freemediatype">FreeMediaType</a> helper function.

If the pin is not connected, this method clears the media type specified by <i>pmt</i> and returns an error code.

## -see-also

<a href="/windows/desktop/DirectShow/data-flow-in-the-filter-graph">Data Flow in the Filter Graph</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ipin">IPin Interface</a>