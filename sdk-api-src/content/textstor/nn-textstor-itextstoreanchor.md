---
UID: NN:textstor.ITextStoreAnchor
title: ITextStoreAnchor (textstor.h)
description: The ITextStoreAnchor interface is implemented by a Microsoft Active Accessibility client and is used by the TSF manager to manipulate text streams.
helpviewer_keywords: ["ITextStoreAnchor","ITextStoreAnchor interface [Text Services Framework]","ITextStoreAnchor interface [Text Services Framework]","described","_tsf_itextstoreanchor_ref","textstor/ITextStoreAnchor","tsf.itextstoreanchor"]
old-location: tsf\itextstoreanchor.htm
tech.root: TSF
ms.assetid: 62730a6d-4dc8-4207-9818-ab95e6537854
ms.date: 12/05/2018
ms.keywords: ITextStoreAnchor, ITextStoreAnchor interface [Text Services Framework], ITextStoreAnchor interface [Text Services Framework],described, _tsf_itextstoreanchor_ref, textstor/ITextStoreAnchor, tsf.itextstoreanchor
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
 - ITextStoreAnchor
 - textstor/ITextStoreAnchor
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
 - ITextStoreAnchor
---

# ITextStoreAnchor interface


## -description

The ITextStoreAnchor interface is implemented by a <a href="/previous-versions/ms971350(v=msdn.10)">Microsoft Active Accessibility</a> client and is used by the TSF manager to manipulate text streams. <a href="/windows/desktop/TSF/ranges">Ranges</a> of text within a stream are delimited by <a href="/windows/desktop/TSF/ranges">anchor</a> objects. these anchor objects are exposed and manipulated by the <a href="/windows/desktop/api/textstor/nn-textstor-ianchor">IAnchor</a> interface.

An application can obtain an instance of this interface with <a href="/previous-versions/ms971350(v=msdn.10)">Microsoft Active Accessibility</a>. The interface ID is IID_ITextStoreAnchor.

To use the application character position (ACP) model for text manipulation, use <a href="/windows/desktop/api/textstor/nn-textstor-itextstoreacp">ITextStoreACP</a> instead.

## -inheritance

The <b>ITextStoreAnchor</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITextStoreAnchor</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>



<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreacp">ITextStoreACP
      </a>



<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreanchorsink">ITextStoreAnchorSink
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="/previous-versions/ms971350(v=msdn.10)">Microsoft Active Accessibility</a>



<a href="/windows/desktop/TSF/tsviewcookie">TsViewCookie
      </a>
