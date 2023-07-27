---
UID: NF:strmif.IAsyncReader.SyncRead
title: IAsyncReader::SyncRead (strmif.h)
description: The SyncRead method performs a synchronous read. The method blocks until the request is completed. The file positions and the buffer address do not have to be aligned. If the request is not aligned, the method performs a buffered read operation.
helpviewer_keywords: ["IAsyncReader interface [DirectShow]","SyncRead method","IAsyncReader.SyncRead","IAsyncReader::SyncRead","IAsyncReaderSyncRead","SyncRead","SyncRead method [DirectShow]","SyncRead method [DirectShow]","IAsyncReader interface","dshow.iasyncreader_syncread","strmif/IAsyncReader::SyncRead"]
old-location: dshow\iasyncreader_syncread.htm
tech.root: dshow
ms.assetid: 21806449-97b1-4890-9182-a1244c21ba30
ms.date: 4/26/2023
ms.keywords: IAsyncReader interface [DirectShow],SyncRead method, IAsyncReader.SyncRead, IAsyncReader::SyncRead, IAsyncReaderSyncRead, SyncRead, SyncRead method [DirectShow], SyncRead method [DirectShow],IAsyncReader interface, dshow.iasyncreader_syncread, strmif/IAsyncReader::SyncRead
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
 - IAsyncReader::SyncRead
 - strmif/IAsyncReader::SyncRead
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
 - IAsyncReader.SyncRead
---

# IAsyncReader::SyncRead


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SyncRead</code> method performs a synchronous read. The method blocks until the request is completed. The file positions and the buffer address do not have to be aligned. If the request is not aligned, the method performs a buffered read operation.

## -parameters

### -param llPosition [in]

Specifies the byte offset at which to begin reading. The method fails if this value is beyond the end of the file.

### -param lLength [in]

Specifies the number of bytes to read.

### -param pBuffer [out]

Pointer to a buffer that receives the data.

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

This method works even if the filter is stopped.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iasyncreader">IAsyncReader Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iasyncreader-syncreadaligned">IAsyncReader::SyncReadAligned</a>