---
UID: NN:textstor.ITextStoreACPSink
title: ITextStoreACPSink (textstor.h)
description: The ITextStoreACPSink interface is implemented by the TSF manager and is used by an ACP-based application to notify the manager when certain events occur. The manager installs this advise sink by calling ITextStoreACP::AdviseSink.
helpviewer_keywords: ["ITextStoreACPSink","ITextStoreACPSink interface [Text Services Framework]","ITextStoreACPSink interface [Text Services Framework]","described","_tsf_itextstoreacpsink_ref","textstor/ITextStoreACPSink","tsf.itextstoreacpsink"]
old-location: tsf\itextstoreacpsink.htm
tech.root: TSF
ms.assetid: d7e5a04f-7159-436e-a522-4cb63063aeef
ms.date: 12/05/2018
ms.keywords: ITextStoreACPSink, ITextStoreACPSink interface [Text Services Framework], ITextStoreACPSink interface [Text Services Framework],described, _tsf_itextstoreacpsink_ref, textstor/ITextStoreACPSink, tsf.itextstoreacpsink
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITextStoreACPSink
 - textstor/ITextStoreACPSink
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITextStoreACPSink
---

# ITextStoreACPSink interface


## -description

The <b>ITextStoreACPSink</b> interface is implemented by the TSF manager and is used by an ACP-based application to notify the manager when certain events occur. The manager installs this advise sink by calling <a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp-advisesink">ITextStoreACP::AdviseSink</a>.

## -inheritance

The <b>ITextStoreACPSink</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITextStoreACPSink</b> also has these types of members:

## -see-also

<a href="/windows/desktop/TSF/document-locks">Document Locks</a>



<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreacp">ITextStoreACP
      </a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp-advisesink">ITextStoreACP::AdviseSink
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="/windows/desktop/TSF/text-stores">Text Stores</a>
