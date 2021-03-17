---
UID: NF:tom.ITextDocument2.GetDocumentFont
title: ITextDocument2::GetDocumentFont (tom.h)
description: Gets an object that provides the default character format information for this instance of the Text Object Model (TOM) engine.
helpviewer_keywords: ["GetDocumentFont","GetDocumentFont method [Windows Controls]","GetDocumentFont method [Windows Controls]","ITextDocument2 interface","ITextDocument2 interface [Windows Controls]","GetDocumentFont method","ITextDocument2.GetDocumentFont","ITextDocument2::GetDocumentFont","controls.itextdocument2_getdocumentfont","tom/ITextDocument2::GetDocumentFont"]
old-location: controls\itextdocument2_getdocumentfont.htm
tech.root: Controls
ms.assetid: b028c2f6-8c8e-49f8-bf53-f4a639cb16c2
ms.date: 12/05/2018
ms.keywords: GetDocumentFont, GetDocumentFont method [Windows Controls], GetDocumentFont method [Windows Controls],ITextDocument2 interface, ITextDocument2 interface [Windows Controls],GetDocumentFont method, ITextDocument2.GetDocumentFont, ITextDocument2::GetDocumentFont, controls.itextdocument2_getdocumentfont, tom/ITextDocument2::GetDocumentFont
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.dll: Msftedit.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextDocument2::GetDocumentFont
 - tom/ITextDocument2::GetDocumentFont
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextDocument2.GetDocumentFont
---

# ITextDocument2::GetDocumentFont


## -description

Gets an object that provides the default character format information for this instance of the Text Object Model (TOM) engine.

## -parameters

### -param ppFont [out, retval]

Type: <b><a href="/windows/desktop/api/tom/nn-tom-itextfont2">ITextFont2</a>**</b>

The object that provides the default character format information.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextdocument2">ITextDocument2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextdocument2-setdocumentfont">ITextDocument2::SetDocumentFont</a>