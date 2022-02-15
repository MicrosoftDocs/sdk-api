---
UID: NN:textstor.ITextStoreAnchorSink
title: ITextStoreAnchorSink (textstor.h)
description: The ITextStoreAnchorSink interface is implemented by the TSF manager and is used by an anchor-based application to notify the manager when certain events occur. The manager installs this advise sink by calling ITextStoreAnchor::AdviseSink.
helpviewer_keywords: ["ITextStoreAnchorSink","ITextStoreAnchorSink interface [Text Services Framework]","ITextStoreAnchorSink interface [Text Services Framework]","described","_tsf_itextstoreanchorsink_ref","textstor/ITextStoreAnchorSink","tsf.itextstoreanchorsink"]
old-location: tsf\itextstoreanchorsink.htm
tech.root: TSF
ms.assetid: fb96b4fb-864f-4f32-bf7c-cf7f199e552a
ms.date: 12/05/2018
ms.keywords: ITextStoreAnchorSink, ITextStoreAnchorSink interface [Text Services Framework], ITextStoreAnchorSink interface [Text Services Framework],described, _tsf_itextstoreanchorsink_ref, textstor/ITextStoreAnchorSink, tsf.itextstoreanchorsink
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
 - ITextStoreAnchorSink
 - textstor/ITextStoreAnchorSink
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
 - ITextStoreAnchorSink
---

# ITextStoreAnchorSink interface


## -description

The <b>ITextStoreAnchorSink</b> interface is implemented by the TSF manager and is used by an anchor-based application to notify the manager when certain events occur. The manager installs this advise sink by calling <a href="/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-advisesink">ITextStoreAnchor::AdviseSink</a>.

The interface ID is IID_ITextStoreAnchorSink.

## -inheritance

The <b>ITextStoreAnchorSink</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITextStoreAnchorSink</b> also has these types of members:

## -see-also

<a href="/windows/desktop/TSF/document-locks">Document Locks</a>



<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreanchor">ITextStoreAnchor
      </a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-advisesink">ITextStoreAnchor::AdviseSink
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="/windows/desktop/TSF/text-stores">Text Stores</a>
