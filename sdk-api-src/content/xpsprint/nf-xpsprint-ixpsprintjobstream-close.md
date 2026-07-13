---
UID: NF:xpsprint.IXpsPrintJobStream.Close
title: IXpsPrintJobStream::Close (xpsprint.h)
description: Closes the stream and indicates to the print job that the entire document has been written to the print queue by the application.
helpviewer_keywords: ["Close","Close method [Windows GDI]","Close method [Windows GDI]","IXpsPrintJobStream interface","IXpsPrintJobStream interface [Windows GDI]","Close method","IXpsPrintJobStream.Close","IXpsPrintJobStream::Close","gdi.ixpsprintjobstream_close","xpsprint/IXpsPrintJobStream::Close"]
old-location: gdi\ixpsprintjobstream_close.htm
tech.root: xps
ms.assetid: 259d0224-4e6e-43c8-905d-3529c781986a
ms.date: 12/05/2018
ms.keywords: Close, Close method [Windows GDI], Close method [Windows GDI],IXpsPrintJobStream interface, IXpsPrintJobStream interface [Windows GDI],Close method, IXpsPrintJobStream.Close, IXpsPrintJobStream::Close, gdi.ixpsprintjobstream_close, xpsprint/IXpsPrintJobStream::Close
req.header: xpsprint.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXpsPrintJobStream::Close
 - xpsprint/IXpsPrintJobStream::Close
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - XpsPrint.h
api_name:
 - IXpsPrintJobStream.Close
---

# IXpsPrintJobStream::Close


## -description

<p class="CCE_Message">[IXpsPrintJobStream::Close is not supported and may be altered or unavailable in the future. ]

Closes the stream and indicates to the print job that the entire document has been written to the print queue by the application.



## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

After <b>Close</b> has been called, all subsequent attempts to write data to the stream will fail.

## -see-also

<a href="/previous-versions/windows/desktop/dd316975(v=vs.85)">Documents</a>



<a href="/windows/desktop/api/xpsprint/nn-xpsprint-ixpsprintjobstream">IXpsPrintJobStream</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>
