---
UID: NF:textstor.ITextStoreACP2.InsertTextAtSelection
title: ITextStoreACP2::InsertTextAtSelection (textstor.h)
description: Inserts text at the insertion point or selection. A caller must have a read/write lock on the document before inserting text.
helpviewer_keywords: ["ITextStoreACP2 interface [Text Services Framework]","InsertTextAtSelection method","ITextStoreACP2.InsertTextAtSelection","ITextStoreACP2::InsertTextAtSelection","InsertTextAtSelection","InsertTextAtSelection method [Text Services Framework]","InsertTextAtSelection method [Text Services Framework]","ITextStoreACP2 interface","textstor/ITextStoreACP2::InsertTextAtSelection","tsf.itextstoreacp2_inserttextatselection"]
old-location: tsf\itextstoreacp2_inserttextatselection.htm
tech.root: TSF
ms.assetid: 5e1e0893-53be-4753-ba49-32e69597a130
ms.date: 12/05/2018
ms.keywords: ITextStoreACP2 interface [Text Services Framework],InsertTextAtSelection method, ITextStoreACP2.InsertTextAtSelection, ITextStoreACP2::InsertTextAtSelection, InsertTextAtSelection, InsertTextAtSelection method [Text Services Framework], InsertTextAtSelection method [Text Services Framework],ITextStoreACP2 interface, textstor/ITextStoreACP2::InsertTextAtSelection, tsf.itextstoreacp2_inserttextatselection
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextStoreACP2::InsertTextAtSelection
 - textstor/ITextStoreACP2::InsertTextAtSelection
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
 - ITextStoreACP2.InsertTextAtSelection
---

# ITextStoreACP2::InsertTextAtSelection


## -description

Inserts text at the insertion point or selection. A caller must have a read/write lock on the document before inserting text.

## -parameters

### -param dwFlags [in]

### -param pchText [in]

### -param cch [in]

### -param pacpStart [out]

### -param pacpEnd [out]

### -param pChange [out]

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The values of the <i>pacpStart</i> and the <i>pacpEnd</i> parameters depend upon how the client application inserts text into a document. For example, if the application sets the cursor at the start of the inserted text after text insertion, then the value for the <i>pacpStart</i> and <i>pacpEnd</i> parameters is the same as the <b>acpStart</b> member of the <a href="/windows/desktop/api/textstor/ns-textstor-ts_textchange">TS_TEXTCHANGE</a> structure.

Applications should not call the <a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacpsink-ontextchange">OnTextChange</a> method in response to this method.

## -see-also

<a href="/windows/desktop/TSF/compositions">Compositions</a>



<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreacp2">ITextStoreACP2</a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacpsink-ontextchange">OnTextChange</a>



<a href="/windows/desktop/TSF/tf-ias--constants">TF_IAS_* Constants
      </a>



<a href="/windows/desktop/api/textstor/ns-textstor-ts_textchange">TS_TEXTCHANGE</a>