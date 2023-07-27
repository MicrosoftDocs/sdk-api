---
UID: NF:strmif.IPin.EndOfStream
title: IPin::EndOfStream (strmif.h)
description: The EndOfStream method notifies the pin that no additional data is expected, until a new run command is issued to the filter.
helpviewer_keywords: ["EndOfStream","EndOfStream method [DirectShow]","EndOfStream method [DirectShow]","IPin interface","IPin interface [DirectShow]","EndOfStream method","IPin.EndOfStream","IPin::EndOfStream","IPinEndOfStream","dshow.ipin_endofstream","strmif/IPin::EndOfStream"]
old-location: dshow\ipin_endofstream.htm
tech.root: dshow
ms.assetid: b0cca250-9603-4d58-8af5-5b272730e5fa
ms.date: 4/26/2023
ms.keywords: EndOfStream, EndOfStream method [DirectShow], EndOfStream method [DirectShow],IPin interface, IPin interface [DirectShow],EndOfStream method, IPin.EndOfStream, IPin::EndOfStream, IPinEndOfStream, dshow.ipin_endofstream, strmif/IPin::EndOfStream
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
 - IPin::EndOfStream
 - strmif/IPin::EndOfStream
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
 - IPin.EndOfStream
---

# IPin::EndOfStream


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>EndOfStream</code> method notifies the pin that no additional data is expected, until a new run command is issued to the filter.



Applications should not call this method. This method is called by other filters to signal the end of the stream.



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

This method sends an end-of-stream notification to the pin. The pin delivers the notification downstream. It must serialize end-of-stream notifications with <a href="/windows/desktop/api/strmif/nf-strmif-imeminputpin-receive">IMemInputPin::Receive</a> calls. If the pin queues media samples for delivery, it should queue end-of-stream notifications as well. The <a href="/windows/desktop/api/strmif/nf-strmif-ipin-beginflush">IPin::BeginFlush</a> method flushes any queued end-of-stream notifications.

## -see-also

<a href="/windows/desktop/DirectShow/data-flow-in-the-filter-graph">Data Flow in the Filter Graph</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ipin">IPin Interface</a>
