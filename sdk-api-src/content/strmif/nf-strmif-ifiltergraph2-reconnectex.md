---
UID: NF:strmif.IFilterGraph2.ReconnectEx
title: IFilterGraph2::ReconnectEx (strmif.h)
description: The ReconnectEx method breaks the existing pin connection and reconnects it to the same pin, using a specified media type.
helpviewer_keywords: ["IFilterGraph2 interface [DirectShow]","ReconnectEx method","IFilterGraph2.ReconnectEx","IFilterGraph2::ReconnectEx","IFilterGraph2ReconnectEx","ReconnectEx","ReconnectEx method [DirectShow]","ReconnectEx method [DirectShow]","IFilterGraph2 interface","dshow.ifiltergraph2_reconnectex","strmif/IFilterGraph2::ReconnectEx"]
old-location: dshow\ifiltergraph2_reconnectex.htm
tech.root: dshow
ms.assetid: a72cf427-056b-4751-9c4a-665251e549f8
ms.date: 4/26/2023
ms.keywords: IFilterGraph2 interface [DirectShow],ReconnectEx method, IFilterGraph2.ReconnectEx, IFilterGraph2::ReconnectEx, IFilterGraph2ReconnectEx, ReconnectEx, ReconnectEx method [DirectShow], ReconnectEx method [DirectShow],IFilterGraph2 interface, dshow.ifiltergraph2_reconnectex, strmif/IFilterGraph2::ReconnectEx
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
 - IFilterGraph2::ReconnectEx
 - strmif/IFilterGraph2::ReconnectEx
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
 - IFilterGraph2.ReconnectEx
---

# IFilterGraph2::ReconnectEx


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>ReconnectEx</code> method breaks the existing pin connection and reconnects it to the same pin, using a specified media type.



Applications should not call this method. It is called by filters during the graph building process.

## -parameters

### -param ppin [in]

Pointer to the pin to disconnect and reconnect.

### -param pmt [in]

Pointer to the media type to reconnect with. Specify <b>NULL</b> to use the existing media type.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Pin was not connected. No error.

</td>
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
<dt><b>VFW_E_NOT_STOPPED</b></dt>
</dl>
</td>
<td width="60%">
The filter is not stopped, but it does not support reconnection while in a running state.

</td>
</tr>
</table>

## -remarks

Filters can call this method in order to renegotiate a pin connection. The method executes on a separate thread. Before calling this method, call <a href="/windows/desktop/api/strmif/nf-strmif-ipin-queryaccept">IPin::QueryAccept</a> on the other pin to ensure that the reconnection attempt will succeed. Do not call this method unless <b>QueryAccept</b> returns S_OK. Otherwise, because the reconnection is performed asynchronously, the reconnection might fail even though the <code>ReconnectEx</code> method succeeds, leaving the filter graph in an inconsistent state.

This method improves on the <a href="/windows/desktop/api/strmif/nf-strmif-ifiltergraph-reconnect">IFilterGraph::Reconnect</a> method by specifying a media type. This makes the reconnection more likely to succeed.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ifiltergraph2">IFilterGraph2 Interface</a>



<a href="/windows/desktop/DirectShow/reconnecting-pins">Reconnecting Pins</a>