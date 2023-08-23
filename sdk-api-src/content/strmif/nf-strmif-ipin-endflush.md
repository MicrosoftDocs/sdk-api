---
UID: NF:strmif.IPin.EndFlush
title: IPin::EndFlush (strmif.h)
description: The EndFlush method ends a flush operation. (IPin.EndFlush)
helpviewer_keywords: ["EndFlush","EndFlush method [DirectShow]","EndFlush method [DirectShow]","IPin interface","IPin interface [DirectShow]","EndFlush method","IPin.EndFlush","IPin::EndFlush","IPinEndFlush","dshow.ipin_endflush","strmif/IPin::EndFlush"]
old-location: dshow\ipin_endflush.htm
tech.root: dshow
ms.assetid: 42b201b6-1fbf-4a01-aed7-23a9e66c11ea
ms.date: 4/26/2023
ms.keywords: EndFlush, EndFlush method [DirectShow], EndFlush method [DirectShow],IPin interface, IPin interface [DirectShow],EndFlush method, IPin.EndFlush, IPin::EndFlush, IPinEndFlush, dshow.ipin_endflush, strmif/IPin::EndFlush
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
 - IPin::EndFlush
 - strmif/IPin::EndFlush
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
 - IPin.EndFlush
---

# IPin::EndFlush


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>EndFlush</code> method ends a flush operation.



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

When this method is called, the filter performs the following actions:

<ol>
<li>Waits for all queued samples to be discarded.</li>
<li>Frees any buffered data, including any pending end-of-stream notifications.</li>
<li>Clears any pending <a href="/windows/desktop/DirectShow/ec-complete">EC_COMPLETE</a> notifications.</li>
<li>Calls <code>EndFlush</code> downstream.</li>
</ol>
When the method returns, the pin can accept new samples.

## -see-also

<a href="/windows/desktop/DirectShow/data-flow-in-the-filter-graph">Data Flow in the Filter Graph</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ipin">IPin Interface</a>
