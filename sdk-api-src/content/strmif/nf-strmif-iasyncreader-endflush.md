---
UID: NF:strmif.IAsyncReader.EndFlush
title: IAsyncReader::EndFlush (strmif.h)
description: The EndFlush method ends a flush operation. (IAsyncReader.EndFlush)
helpviewer_keywords: ["EndFlush","EndFlush method [DirectShow]","EndFlush method [DirectShow]","IAsyncReader interface","IAsyncReader interface [DirectShow]","EndFlush method","IAsyncReader.EndFlush","IAsyncReader::EndFlush","IAsyncReaderEndFlush","dshow.iasyncreader_endflush","strmif/IAsyncReader::EndFlush"]
old-location: dshow\iasyncreader_endflush.htm
tech.root: dshow
ms.assetid: 38a7fd8a-c027-49fd-8f52-49ddf072fe02
ms.date: 4/26/2023
ms.keywords: EndFlush, EndFlush method [DirectShow], EndFlush method [DirectShow],IAsyncReader interface, IAsyncReader interface [DirectShow],EndFlush method, IAsyncReader.EndFlush, IAsyncReader::EndFlush, IAsyncReaderEndFlush, dshow.iasyncreader_endflush, strmif/IAsyncReader::EndFlush
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
 - IAsyncReader::EndFlush
 - strmif/IAsyncReader::EndFlush
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
 - IAsyncReader.EndFlush
---

# IAsyncReader::EndFlush


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>EndFlush</code> method ends a flush operation.



## -returns

Returns S_OK if successful, or S_FALSE otherwise.

## -remarks

While the pin is flushing, the <a href="/windows/desktop/api/strmif/nf-strmif-iasyncreader-request">IAsyncReader::Request</a> method fails and the <a href="/windows/desktop/api/strmif/nf-strmif-iasyncreader-waitfornext">IAsyncReader::WaitForNext</a> method returns immediately. Call the <code>EndFlush</code> method at the end of a flush operation, to reenable the <b>Request</b> method.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iasyncreader">IAsyncReader Interface</a>
