---
UID: NF:strmif.IAsyncReader.Request
title: IAsyncReader::Request (strmif.h)
description: The Request method queues an asynchronous request for data.
helpviewer_keywords: ["IAsyncReader interface [DirectShow]","Request method","IAsyncReader.Request","IAsyncReader::Request","IAsyncReaderRequest","Request","Request method [DirectShow]","Request method [DirectShow]","IAsyncReader interface","dshow.iasyncreader_request","strmif/IAsyncReader::Request"]
old-location: dshow\iasyncreader_request.htm
tech.root: dshow
ms.assetid: d0eab370-bb17-48fa-9926-6a6eeaba5603
ms.date: 4/26/2023
ms.keywords: IAsyncReader interface [DirectShow],Request method, IAsyncReader.Request, IAsyncReader::Request, IAsyncReaderRequest, Request, Request method [DirectShow], Request method [DirectShow],IAsyncReader interface, dshow.iasyncreader_request, strmif/IAsyncReader::Request
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
 - IAsyncReader::Request
 - strmif/IAsyncReader::Request
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
 - IAsyncReader.Request
---

# IAsyncReader::Request


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>Request</code> method queues an asynchronous request for data.

## -parameters

### -param pSample

Pointer to the <a href="/windows/desktop/api/strmif/nn-strmif-imediasample">IMediaSample</a> interface of a media sample provided by the caller.

### -param dwUser [in]

Specifies an arbitrary value that is returned when the request completes.

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
<dt><b>VFW_E_BADALIGN</b></dt>
</dl>
</td>
<td width="60%">
The buffer is not aligned correctly.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_SAMPLE_TIME_NOT_SET</b></dt>
</dl>
</td>
<td width="60%">
The sample was not time stamped.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
The pin is flushing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_HANDLE_EOF)</b></dt>
</dl>
</td>
<td width="60%">
The requested start position is past the end of the file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
</table>

## -remarks

Before calling this method, retrieve a media sample from the pin's allocator. Time stamp the sample with the byte offsets you are requesting, first and last inclusive, multiplied by 10,000,000. Byte offsets are relative to the start of the stream.

The start and stop positions should match the alignment that was decided when the pins connected. Otherwise, the method might return VFW_E_BADALIGN. If the agreed alignment is coarser than the actual alignment of the stream, the stop position might exceed the real duration. If so, the method rounds the stop position down to the actual alignment.

Although it is technically a violation of COM rules, the caller must leave an outstanding reference count on the sample. The <code>Request</code> method does not call <b>AddRef</b> or <b>Release</b>, so the reference count is needed to keep the sample active.

The method returns before the request completes. Call the <a href="/windows/desktop/api/strmif/nf-strmif-iasyncreader-waitfornext">IAsyncReader::WaitForNext</a> method to wait for the request. Do not reuse the original media sample while the request is pending. The <b>WaitForNext</b> method returns a pointer to the original sample. If the request succeeded, the sample contains the requested data. The <b>WaitForNext</b> method also returns whatever value is specified in the <i>dwUser</i> parameter. The caller can use this value to identify the sample.


#### Examples

The following example shows a possible helper function for an input pin, to queue requests:

<div class="code"><span><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>

```
CMyPin::QueueSample(long cbFirst, long cbLast, DWORD_PTR dwuser)
{
    IMediaSample* pSample = NULL;
    HRESULT hr = m_pAlloc->GetBuffer(&pSample, NULL, NULL, 0);
    if (FAILED(hr)) 
    { 
        return hr; 
    }

    LONGLONG tStart = cbFirst * 10000000, tStop = cbLast * 10000000;
    hr = pSample->SetTime(&tStart, &tStop);
    if (SUCCEEDED(hr))
    {
        hr = m_pReader->Request(pSample, dwuser);
    }

    if (FAILED(hr))
    {
        pSample->Release();
    }
    return hr;
}
```
</td>
</tr>
</table></span></div>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iasyncreader">IAsyncReader Interface</a>