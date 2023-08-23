---
UID: NF:strmif.IPin.Disconnect
title: IPin::Disconnect (strmif.h)
description: The Disconnect method breaks the current pin connection.
helpviewer_keywords: ["Disconnect","Disconnect method [DirectShow]","Disconnect method [DirectShow]","IPin interface","IPin interface [DirectShow]","Disconnect method","IPin.Disconnect","IPin::Disconnect","IPinDisconnect","dshow.ipin_disconnect","strmif/IPin::Disconnect"]
old-location: dshow\ipin_disconnect.htm
tech.root: dshow
ms.assetid: 46e1e99c-848b-4936-b6bf-4ef1703a1f42
ms.date: 4/26/2023
ms.keywords: Disconnect, Disconnect method [DirectShow], Disconnect method [DirectShow],IPin interface, IPin interface [DirectShow],Disconnect method, IPin.Disconnect, IPin::Disconnect, IPinDisconnect, dshow.ipin_disconnect, strmif/IPin::Disconnect
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
 - IPin::Disconnect
 - strmif/IPin::Disconnect
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
 - IPin.Disconnect
---

# IPin::Disconnect


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>Disconnect</code> method breaks the current pin connection.



The Filter Graph Manager calls this method when it disconnects two filters. Applications and filters should not call this method. Instead, call the <a href="/windows/desktop/api/strmif/nf-strmif-ifiltergraph-disconnect">IFilterGraph::Disconnect</a> method on the Filter Graph Manager.



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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The pin was not connected.

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
<dt><b>VFW_E_NOT_STOPPED</b></dt>
</dl>
</td>
<td width="60%">
The filter is active.

</td>
</tr>
</table>

## -remarks

This method fails if the filter is paused or running. If the pin supports the <a href="/windows/desktop/api/strmif/nn-strmif-ipinconnection">IPinConnection</a> interface, call <a href="/windows/desktop/api/strmif/nf-strmif-ipinconnection-dynamicdisconnect">IPinConnection::DynamicDisconnect</a> to disconnect the pin when the filter is paused or running.

This method does not disconnect the other pin in the pin connection.

## -see-also

<a href="/windows/desktop/DirectShow/data-flow-in-the-filter-graph">Data Flow in the Filter Graph</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ipin">IPin Interface</a>
