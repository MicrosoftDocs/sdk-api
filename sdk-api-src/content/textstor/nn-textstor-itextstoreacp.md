---
UID: NN:textstor.ITextStoreACP
title: ITextStoreACP (textstor.h)
description: The ITextStoreACP interface is implemented by the application and is used by the TSF manager to manipulate text streams or text stores in TSF.
helpviewer_keywords: ["ITextStoreACP","ITextStoreACP interface [Text Services Framework]","ITextStoreACP interface [Text Services Framework]","described","_tsf_itextstoreacp_ref","textstor/ITextStoreACP","tsf.itextstoreacp"]
old-location: tsf\itextstoreacp.htm
tech.root: TSF
ms.assetid: 21e011f7-6791-4eb9-85c9-18bd10107119
ms.date: 12/05/2018
ms.keywords: ITextStoreACP, ITextStoreACP interface [Text Services Framework], ITextStoreACP interface [Text Services Framework],described, _tsf_itextstoreacp_ref, textstor/ITextStoreACP, tsf.itextstoreacp
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - ITextStoreACP
 - textstor/ITextStoreACP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITextStoreACP
---

# ITextStoreACP interface


## -description

The <b>ITextStoreACP</b> interface is implemented by the application and is used by the TSF manager to manipulate text streams or text stores in TSF. An application can obtain an instance of this interface with a call to the <a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext</a> method. The interface ID is IID_ITextStoreACP.

This interface exposes text stores through an application character position (ACP) format. Applications that use an anchor-based format should use <a href="/windows/desktop/api/textstor/nn-textstor-itextstoreanchor">ITextStoreAnchor</a>.

## -inheritance

The <b>ITextStoreACP</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITextStoreACP</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="/windows/desktop/TSF/text-stores">Text Stores</a>
