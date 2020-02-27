---
UID: NF:strmif.IAsyncReader.EndFlush
title: IAsyncReader::EndFlush (strmif.h)
description: The EndFlush method ends a flush operation.
old-location: dshow\iasyncreader_endflush.htm
tech.root: DirectShow
ms.assetid: 38a7fd8a-c027-49fd-8f52-49ddf072fe02
ms.date: 12/05/2018
ms.keywords: EndFlush, EndFlush method [DirectShow], EndFlush method [DirectShow],IAsyncReader interface, IAsyncReader interface [DirectShow],EndFlush method, IAsyncReader.EndFlush, IAsyncReader::EndFlush, IAsyncReaderEndFlush, dshow.iasyncreader_endflush, strmif/IAsyncReader::EndFlush
f1_keywords:
- strmif/IAsyncReader.EndFlush
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAsyncReader::EndFlush


## -description



The <code>EndFlush</code> method ends a flush operation.




## -parameters






## -returns



Returns S_OK if successful, or S_FALSE otherwise.




## -remarks



While the pin is flushing, the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iasyncreader-request">IAsyncReader::Request</a> method fails and the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iasyncreader-waitfornext">IAsyncReader::WaitForNext</a> method returns immediately. Call the <code>EndFlush</code> method at the end of a flush operation, to reenable the <b>Request</b> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iasyncreader">IAsyncReader Interface</a>
 

 

