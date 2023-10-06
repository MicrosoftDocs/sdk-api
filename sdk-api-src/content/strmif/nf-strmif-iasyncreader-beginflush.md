---
UID: NF:strmif.IAsyncReader.BeginFlush
title: IAsyncReader::BeginFlush (strmif.h)
description: The BeginFlush method begins a flush operation. (IAsyncReader.BeginFlush)
helpviewer_keywords: ["BeginFlush","BeginFlush method [DirectShow]","BeginFlush method [DirectShow]","IAsyncReader interface","IAsyncReader interface [DirectShow]","BeginFlush method","IAsyncReader.BeginFlush","IAsyncReader::BeginFlush","IAsyncReaderBeginFlush","dshow.iasyncreader_beginflush","strmif/IAsyncReader::BeginFlush"]
old-location: dshow\iasyncreader_beginflush.htm
tech.root: dshow
ms.assetid: 29153592-dbc1-42b4-bd4e-2f1aef8d4c19
ms.date: 4/26/2023
ms.keywords: BeginFlush, BeginFlush method [DirectShow], BeginFlush method [DirectShow],IAsyncReader interface, IAsyncReader interface [DirectShow],BeginFlush method, IAsyncReader.BeginFlush, IAsyncReader::BeginFlush, IAsyncReaderBeginFlush, dshow.iasyncreader_beginflush, strmif/IAsyncReader::BeginFlush
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
 - IAsyncReader::BeginFlush
 - strmif/IAsyncReader::BeginFlush
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
 - IAsyncReader.BeginFlush
---

# IAsyncReader::BeginFlush


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>BeginFlush</code> method begins a flush operation.



## -returns

Returns S_OK if successful, or S_FALSE otherwise.

## -remarks

This method interrupts all pending read requests. While the pin is flushing, the <a href="/windows/desktop/api/strmif/nf-strmif-iasyncreader-request">IAsyncReader::Request</a> method fails and the <a href="/windows/desktop/api/strmif/nf-strmif-iasyncreader-waitfornext">IAsyncReader::WaitForNext</a> method returns immediately, possibly with the return code VFW_E_TIMEOUT.

The downstream input pin should call this method whenever the downstream filter flushes the filter graph. After calling this method, call the <b>WaitForNext</b> method until it returns <b>NULL</b> in the <i>ppSample</i> parameter, to clear out the queue of pending samples. Ignore error codes, and release each sample. Then call the <a href="/windows/desktop/api/strmif/nf-strmif-iasyncreader-endflush">IAsyncReader::EndFlush</a> method to end the flush operation.

For more information, see <a href="/windows/desktop/DirectShow/flushing">Flushing</a>.


#### Examples

The following example shows how a downstream input pin should call this method:

<div class="code"><span><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
m_pReader-&gt;BeginFlush(); 
while (1) {
    IMediaSample *pSample;
    DWORD_PTR dwUnused;
    m_pReader-&gt;WaitForNext(0, &amp;pSample, &amp;dwUnused);
    if(pSample) { 
        pSample-&gt;Release();  
    } 
    else {  // No more samples.
        break;
    }
}
m_pReader-&gt;EndFlush();
</pre>
</td>
</tr>
</table></span></div>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iasyncreader">IAsyncReader Interface</a>
