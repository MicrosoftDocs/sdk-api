---
UID: NN:xpsprint.IXpsPrintJobStream
title: IXpsPrintJobStream (xpsprint.h)
description: A write-only stream interface into which an application writes print job data.
helpviewer_keywords: ["IXpsPrintJobStream","IXpsPrintJobStream interface [Windows GDI]","IXpsPrintJobStream interface [Windows GDI]","described","gdi.ixpsprintjobstream","xpsprint/IXpsPrintJobStream"]
old-location: gdi\ixpsprintjobstream.htm
tech.root: xps
ms.assetid: a7855015-32db-48ff-8f8d-3d84d2843fde
ms.date: 12/05/2018
ms.keywords: IXpsPrintJobStream, IXpsPrintJobStream interface [Windows GDI], IXpsPrintJobStream interface [Windows GDI],described, gdi.ixpsprintjobstream, xpsprint/IXpsPrintJobStream
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
 - IXpsPrintJobStream
 - xpsprint/IXpsPrintJobStream
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
 - IXpsPrintJobStream
---

# IXpsPrintJobStream interface


## -description

<p class="CCE_Message">[IXpsPrintJobStream is not supported and may be altered or unavailable in the future. ]

A write-only stream interface into which an application writes print job data.

## -inheritance

The <b>IXpsPrintJobStream</b> interface inherits from <a href="/windows/desktop/api/objidl/nn-objidl-isequentialstream">ISequentialStream</a>. <b>IXpsPrintJobStream</b> also has these types of members:

## -remarks

<div class="alert"><b>Note</b>  The <a href="/windows/desktop/api/xpsprint/nf-xpsprint-ixpsprintjobstream-close">Close</a> method must be called before this interface is released.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/dd316975(v=vs.85)">Documents</a>



<a href="/windows/desktop/api/objidl/nn-objidl-isequentialstream">ISequentialStream</a>



<a href="/windows/desktop/api/xpsprint/nn-xpsprint-ixpsprintjob">IXpsPrintJob</a>



<a href="/windows/desktop/api/xpsprint/nf-xpsprint-startxpsprintjob">StartXpsPrintJob</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>
