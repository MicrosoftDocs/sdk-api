---
UID: NF:strmif.IAsyncReader.WaitForNext
title: IAsyncReader::WaitForNext (strmif.h)
description: The WaitForNext method waits for the next pending read request to complete.
helpviewer_keywords: ["IAsyncReader interface [DirectShow]","WaitForNext method","IAsyncReader.WaitForNext","IAsyncReader::WaitForNext","IAsyncReaderWaitForNext","WaitForNext","WaitForNext method [DirectShow]","WaitForNext method [DirectShow]","IAsyncReader interface","dshow.iasyncreader_waitfornext","strmif/IAsyncReader::WaitForNext"]
old-location: dshow\iasyncreader_waitfornext.htm
tech.root: dshow
ms.assetid: fc54f917-3b86-4c0b-b356-217bc9793504
ms.date: 4/26/2023
ms.keywords: IAsyncReader interface [DirectShow],WaitForNext method, IAsyncReader.WaitForNext, IAsyncReader::WaitForNext, IAsyncReaderWaitForNext, WaitForNext, WaitForNext method [DirectShow], WaitForNext method [DirectShow],IAsyncReader interface, dshow.iasyncreader_waitfornext, strmif/IAsyncReader::WaitForNext
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
 - IAsyncReader::WaitForNext
 - strmif/IAsyncReader::WaitForNext
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
 - IAsyncReader.WaitForNext
---

# IAsyncReader::WaitForNext


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>WaitForNext</code> method waits for the next pending read request to complete.

## -parameters

### -param dwTimeout [in]

Specifies a time-out in milliseconds. Use the value INFINITE to wait indefinitely

### -param ppSample [out]

Address of a variable that receives an <a href="/windows/desktop/api/strmif/nn-strmif-imediasample">IMediaSample</a> interface pointer.

### -param pdwUser [out]

Pointer to a variable that receives the value of the <i>dwUser</i> parameter specified in the <a href="/windows/desktop/api/strmif/nf-strmif-iasyncreader-request">IAsyncReader::Request</a> method.

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
<dt><b>VFW_E_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The time-out expired, or the pin is flushing.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
A read error occurred.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Reached the end of the file; retrieved fewer bytes than requested.

</td>
</tr>
</table>

## -remarks

If the method succeeds, the <i>ppSample</i> parameter contains a pointer to a media sample, whose buffer holds the requested data. Call the <a href="/windows/desktop/api/strmif/nf-strmif-imediasample-gettime">IMediaSample::GetTime</a> method and divide the results by 10,000,000 to determine the start and stop bytes. Samples may be returned out of order. Release the sample when you are finished processing the data.

The method fails if the pin is flushing. However, it may return an empty sample in <i>ppSample</i>. If <i>*ppSample</i> is non-<b>NULL</b>, release the sample and discard it. For more information, see <a href="/windows/desktop/api/strmif/nf-strmif-iasyncreader-beginflush">IAsyncReader::BeginFlush</a>.

If a read error occurs, the source filter sends an error event to the Filter Graph Manager; the caller does not have to signal an error.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iasyncreader">IAsyncReader Interface</a>