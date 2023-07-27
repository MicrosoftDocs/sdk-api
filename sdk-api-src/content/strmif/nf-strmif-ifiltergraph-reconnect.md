---
UID: NF:strmif.IFilterGraph.Reconnect
title: IFilterGraph::Reconnect (strmif.h)
description: The Reconnect method disconnects a pin and then reconnects it to the same pin.
helpviewer_keywords: ["IFilterGraph interface [DirectShow]","Reconnect method","IFilterGraph.Reconnect","IFilterGraph::Reconnect","IFilterGraphReconnect","Reconnect","Reconnect method [DirectShow]","Reconnect method [DirectShow]","IFilterGraph interface","dshow.ifiltergraph_reconnect","strmif/IFilterGraph::Reconnect"]
old-location: dshow\ifiltergraph_reconnect.htm
tech.root: dshow
ms.assetid: 98a46014-031b-4f35-b1bc-58aef411360b
ms.date: 4/26/2023
ms.keywords: IFilterGraph interface [DirectShow],Reconnect method, IFilterGraph.Reconnect, IFilterGraph::Reconnect, IFilterGraphReconnect, Reconnect, Reconnect method [DirectShow], Reconnect method [DirectShow],IFilterGraph interface, dshow.ifiltergraph_reconnect, strmif/IFilterGraph::Reconnect
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
 - IFilterGraph::Reconnect
 - strmif/IFilterGraph::Reconnect
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
 - IFilterGraph.Reconnect
---

# IFilterGraph::Reconnect


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>Reconnect</code> method disconnects a pin and then reconnects it to the same pin.



Applications should not call this method. It is called by filters during the graph building process.

## -parameters

### -param ppin [in]

Pointer to <a href="/windows/desktop/api/strmif/nn-strmif-ipin">IPin</a> interface of the pin to reconnect.

## -returns

Returns one of the following values.

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
<dt><b>VFW_E_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
Pin is not connected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
Filter is not stopped.

</td>
</tr>
</table>

## -remarks

This method is obsolete; use the <a href="/windows/desktop/api/strmif/nf-strmif-ifiltergraph2-reconnectex">IFilterGraph2::ReconnectEx</a> method instead.

Filters can call this method in order to renegotiate a pin connection. The method executes on a separate thread. Before calling this method, call <a href="/windows/desktop/api/strmif/nf-strmif-ipin-queryaccept">IPin::QueryAccept</a> on the other pin to ensure that the reconnection attempt will succeed. Do not call this method unless <b>QueryAccept</b> returns S_OK. Otherwise, because the reconnection is performed asynchronously, the reconnection might fail even though the <code>Reconnect</code> method succeeds, leaving the filter graph in an inconsistent state.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ifiltergraph">IFilterGraph Interface</a>



<a href="/windows/desktop/DirectShow/reconnecting-pins">Reconnecting Pins</a>