---
UID: NF:strmif.IPin.Connect
title: IPin::Connect (strmif.h)
description: The Connect method connects the pin to another pin.
helpviewer_keywords: ["Connect","Connect method [DirectShow]","Connect method [DirectShow]","IPin interface","IPin interface [DirectShow]","Connect method","IPin.Connect","IPin::Connect","IPinConnect","dshow.ipin_connect","strmif/IPin::Connect"]
old-location: dshow\ipin_connect.htm
tech.root: dshow
ms.assetid: 1b02ee67-5dc5-44c1-bea5-2eab46ebd0f6
ms.date: 4/26/2023
ms.keywords: Connect, Connect method [DirectShow], Connect method [DirectShow],IPin interface, IPin interface [DirectShow],Connect method, IPin.Connect, IPin::Connect, IPinConnect, dshow.ipin_connect, strmif/IPin::Connect
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
 - IPin::Connect
 - strmif/IPin::Connect
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
 - IPin.Connect
---

# IPin::Connect


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>Connect</code> method connects the pin to another pin.



Applications should not call this method. Use <a href="/windows/desktop/api/strmif/nn-strmif-igraphbuilder">IGraphBuilder</a> methods instead. This method is called by the Filter Graph Manager to connect pins.

## -parameters

### -param pReceivePin [in]

Pointer to the receiving pin's <a href="/windows/desktop/api/strmif/nn-strmif-ipin">IPin</a> interface.

### -param pmt [in]

Pointer to an <a href="/windows/desktop/api/strmif/ns-strmif-am_media_type">AM_MEDIA_TYPE</a> structure that specifies the media type for the connection. Can be <b>NULL</b>.

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
<dt><b>VFW_E_ALREADY_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The pin is already connected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NO_ACCEPTABLE_TYPES</b></dt>
</dl>
</td>
<td width="60%">
Cannot find an acceptable media type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NO_TRANSPORT</b></dt>
</dl>
</td>
<td width="60%">
Pins cannot agree on a transport, or there is no allocator for the connection.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_STOPPED</b></dt>
</dl>
</td>
<td width="60%">
The filter is active and the pin does not support dynamic reconnection.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_TYPE_NOT_ACCEPTED</b></dt>
</dl>
</td>
<td width="60%">
The specified media type is not acceptable.

</td>
</tr>
</table>

## -remarks

The <i>pmt</i> parameter can be <b>NULL</b>. It can also specify a partial media type, with a value of GUID_NULL for the major type, subtype, or format.

This method verifies that the connection is possible. If the pin rejects the connection, the method fails. The connecting pin proposes media types by calling <a href="/windows/desktop/api/strmif/nf-strmif-ipin-receiveconnection">IPin::ReceiveConnection</a> on the receiving pin.

## -see-also

<a href="/windows/desktop/DirectShow/data-flow-in-the-filter-graph">Data Flow in the Filter Graph</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ipin">IPin Interface</a>