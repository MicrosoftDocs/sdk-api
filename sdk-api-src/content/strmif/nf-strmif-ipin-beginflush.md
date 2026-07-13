---
UID: NF:strmif.IPin.BeginFlush
title: IPin::BeginFlush (strmif.h)
description: The BeginFlush method begins a flush operation. (IPin.BeginFlush)
helpviewer_keywords: ["BeginFlush","BeginFlush method [DirectShow]","BeginFlush method [DirectShow]","IPin interface","IPin interface [DirectShow]","BeginFlush method","IPin.BeginFlush","IPin::BeginFlush","IPinBeginFlush","dshow.ipin_beginflush","strmif/IPin::BeginFlush"]
old-location: dshow\ipin_beginflush.htm
tech.root: dshow
ms.assetid: 15563666-5f35-46a0-ad12-215979c9d9c1
ms.date: 4/26/2023
ms.keywords: BeginFlush, BeginFlush method [DirectShow], BeginFlush method [DirectShow],IPin interface, IPin interface [DirectShow],BeginFlush method, IPin.BeginFlush, IPin::BeginFlush, IPinBeginFlush, dshow.ipin_beginflush, strmif/IPin::BeginFlush
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
 - IPin::BeginFlush
 - strmif/IPin::BeginFlush
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
 - IPin.BeginFlush
---

# IPin::BeginFlush


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>BeginFlush</code> method begins a flush operation.



Applications should not call this method. This method is called by other filters, to flush data from the graph.



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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The pin is an output pin.

</td>
</tr>
</table>

## -remarks

Call this method only on input pins. Output pins return E_UNEXPECTED.

In a flush operation, a filter discards whatever data it was processing. It rejects new data until the flush is completed. The flush is completed when the upstream pin calls the <a href="/windows/desktop/api/strmif/nf-strmif-ipin-endflush">IPin::EndFlush</a> method. Flushing enables the filter graph to be more responsive when events alter the normal data flow. For example, flushing occurs during a seek.

When <code>BeginFlush</code> is called, the filter performs the following steps:

<ol>
<li>Passes the <code>IPin::BeginFlush</code> call downstream.</li>
<li>Sets an internal flag that causes all data-streaming methods to fail, such as <a href="/windows/desktop/api/strmif/nf-strmif-imeminputpin-receive">IMemInputPin::Receive</a>.</li>
<li>Returns from any blocked calls to the <a href="/windows/desktop/api/strmif/nf-strmif-imeminputpin-receive">Receive</a> method.</li>
</ol>
When the <code>BeginFlush</code> notification reaches a renderer filter, the renderer frees any samples that it holds.

After <code>BeginFlush</code> is called, the pin rejects all samples from upstream, with a return value of S_FALSE, until the <a href="/windows/desktop/api/strmif/nf-strmif-ipin-endflush">IPin::EndFlush</a> method is called.

## -see-also

<a href="/windows/desktop/DirectShow/data-flow-in-the-filter-graph">Data Flow in the Filter Graph</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ipin">IPin Interface</a>
