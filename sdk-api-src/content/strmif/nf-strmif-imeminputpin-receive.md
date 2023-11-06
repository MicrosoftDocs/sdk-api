---
UID: NF:strmif.IMemInputPin.Receive
title: IMemInputPin::Receive (strmif.h)
description: The Receive method receives the next media sample in the stream.
helpviewer_keywords: ["IMemInputPin interface [DirectShow]","Receive method","IMemInputPin.Receive","IMemInputPin::Receive","IMemInputPinReceive","Receive","Receive method [DirectShow]","Receive method [DirectShow]","IMemInputPin interface","dshow.imeminputpin_receive","strmif/IMemInputPin::Receive"]
old-location: dshow\imeminputpin_receive.htm
tech.root: dshow
ms.assetid: 7cc1e57a-a18a-4ea4-9669-0be3fb140d40
ms.date: 4/26/2023
ms.keywords: IMemInputPin interface [DirectShow],Receive method, IMemInputPin.Receive, IMemInputPin::Receive, IMemInputPinReceive, Receive, Receive method [DirectShow], Receive method [DirectShow],IMemInputPin interface, dshow.imeminputpin_receive, strmif/IMemInputPin::Receive
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
 - IMemInputPin::Receive
 - strmif/IMemInputPin::Receive
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
 - IMemInputPin.Receive
---

# IMemInputPin::Receive


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>Receive</code> method receives the next media sample in the stream.

## -parameters

### -param pSample [in]

Pointer to the sample's <a href="/windows/desktop/api/strmif/nn-strmif-imediasample">IMediaSample</a> interface.

## -returns

Returns an <b>HRESULT</b> value. Possible values include those shown in the following table.

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
The sample was rejected.

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
<dt><b>VFW_E_INVALIDMEDIATYPE</b></dt>
</dl>
</td>
<td width="60%">
Invalid media type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_RUNTIME_ERROR</b></dt>
</dl>
</td>
<td width="60%">
A run-time error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
The pin is stopped.

</td>
</tr>
</table>

## -remarks

This method is synchronous and possibly blocking. The pin does one of the following:

<ul>
<li>Rejects the sample.</li>
<li>Returns immediately and processes the sample in a worker thread.</li>
<li>Processes the sample before returning.</li>
</ul>
In the last case, the method might block indefinitely. If this might happen, the <a href="/windows/desktop/api/strmif/nf-strmif-imeminputpin-receivecanblock">IMemInputPin::ReceiveCanBlock</a> method returns S_OK.

If the pin uses a worker thread to process the sample, it holds a reference count on the sample. In any case, the output pin cannot directly re-use this sample. It must call the <a href="/windows/desktop/api/strmif/nf-strmif-imemallocator-getbuffer">IMemAllocator::GetBuffer</a> method to obtain a new sample.

If this method returns S_FALSE or an error code, the upstream filter should stop sending samples until the graph stops or completes a flush operation. Typical reasons for an S_FALSE return value include:

<ul>
<li>The downstream pin is flushing; that is, it received a <b>BeginFlush</b> call and has not yet received an <b>EndFlush</b> call.</li>
<li>The downstream filter detected the end of the stream. (See <a href="/windows/desktop/DirectShow/end-of-stream-notifications">End-of-Stream Notifications</a>.)</li>
</ul>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-imeminputpin">IMemInputPin Interface</a>