---
UID: NF:strmif.IAsyncReader.EndFlush
title: IAsyncReader::EndFlush (strmif.h)
description: The EndFlush method ends a flush operation.
helpviewer_keywords: ["EndFlush","EndFlush method [DirectShow]","EndFlush method [DirectShow]","IAsyncReader interface","IAsyncReader interface [DirectShow]","EndFlush method","IAsyncReader.EndFlush","IAsyncReader::EndFlush","IAsyncReaderEndFlush","dshow.iasyncreader_endflush","strmif/IAsyncReader::EndFlush"]
old-location: dshow\iasyncreader_endflush.htm
tech.root: dshow
ms.assetid: 38a7fd8a-c027-49fd-8f52-49ddf072fe02
ms.date: 12/05/2018
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

The <code>EndFlush</code> method ends a flush operation.



## -returns

Returns S_OK if successful, or S_FALSE otherwise.

## -remarks

While the pin is flushing, the <a href="/windows/desktop/api/strmif/nf-strmif-iasyncreader-request">IAsyncReader::Request</a> method fails and the <a href="/windows/desktop/api/strmif/nf-strmif-iasyncreader-waitfornext">IAsyncReader::WaitForNext</a> method returns immediately. Call the <code>EndFlush</code> method at the end of a flush operation, to reenable the <b>Request</b> method.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iasyncreader">IAsyncReader Interface</a>
