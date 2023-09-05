---
UID: NF:strmif.IAsyncReader.SyncReadAligned
title: IAsyncReader::SyncReadAligned (strmif.h)
description: The SyncReadAligned method performs a synchronous read. The method blocks until the request is completed. The file positions and the buffer address must be aligned; check the allocator properties for the required alignment.
helpviewer_keywords: ["IAsyncReader interface [DirectShow]","SyncReadAligned method","IAsyncReader.SyncReadAligned","IAsyncReader::SyncReadAligned","IAsyncReaderSyncReadAligned","SyncReadAligned","SyncReadAligned method [DirectShow]","SyncReadAligned method [DirectShow]","IAsyncReader interface","dshow.iasyncreader_syncreadaligned","strmif/IAsyncReader::SyncReadAligned"]
old-location: dshow\iasyncreader_syncreadaligned.htm
tech.root: dshow
ms.assetid: 862511f1-7580-44db-aed5-3dd8279dcc33
ms.date: 4/26/2023
ms.keywords: IAsyncReader interface [DirectShow],SyncReadAligned method, IAsyncReader.SyncReadAligned, IAsyncReader::SyncReadAligned, IAsyncReaderSyncReadAligned, SyncReadAligned, SyncReadAligned method [DirectShow], SyncReadAligned method [DirectShow],IAsyncReader interface, dshow.iasyncreader_syncreadaligned, strmif/IAsyncReader::SyncReadAligned
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
 - IAsyncReader::SyncReadAligned
 - strmif/IAsyncReader::SyncReadAligned
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
 - IAsyncReader.SyncReadAligned
---

# IAsyncReader::SyncReadAligned


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SyncReadAligned</code> method performs a synchronous read. The method blocks until the request is completed. The file positions and the buffer address must be aligned; check the allocator properties for the required alignment.

## -parameters

### -param pSample

Pointer to the <a href="/windows/desktop/api/strmif/nn-strmif-imediasample">IMediaSample</a> interface of a media sample provided by the caller.

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
<dt><b>VFW_E_BADALIGN</b></dt>
</dl>
</td>
<td width="60%">
Invalid alignment.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Retrieved fewer bytes than requested. (Probably the end of the file was reached.)

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
</table>

## -remarks

Before calling this method, retrieve a media sample from the pin's allocator. Time stamp the sample with the byte offsets you are requesting, first and last inclusive, multiplied by 10,000,000. Byte offsets are relative to the start of the stream.

The start and stop positions should match the alignment that was decided when the pins connected. Otherwise, the method returns VFW_E_BADALIGN. If the agreed alignment is coarser than the actual alignment of the stream, the stop position might exceed the real duration. If so, the method rounds the stop position down to the actual alignment.

This method performs an unbuffered read, so it might be faster than the <a href="/windows/desktop/api/strmif/nf-strmif-iasyncreader-syncread">IAsyncReader::SyncRead</a> method.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iasyncreader">IAsyncReader Interface</a>