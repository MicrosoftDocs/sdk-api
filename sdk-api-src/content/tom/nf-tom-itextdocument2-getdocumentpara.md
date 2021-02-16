---
UID: NF:tom.ITextDocument2.GetDocumentPara
title: ITextDocument2::GetDocumentPara (tom.h)
description: Gets an object that provides the default paragraph format information for this instance of the Text Object Model (TOM) engine.
helpviewer_keywords: ["GetDocumentPara","GetDocumentPara method [Windows Controls]","GetDocumentPara method [Windows Controls]","ITextDocument2 interface","ITextDocument2 interface [Windows Controls]","GetDocumentPara method","ITextDocument2.GetDocumentPara","ITextDocument2::GetDocumentPara","controls.itextdocument2_getdocumentpara","tom/ITextDocument2::GetDocumentPara"]
old-location: controls\itextdocument2_getdocumentpara.htm
tech.root: Controls
ms.assetid: 3667587e-3cf1-4b86-82fd-2fc34d4cbeee
ms.date: 12/05/2018
ms.keywords: GetDocumentPara, GetDocumentPara method [Windows Controls], GetDocumentPara method [Windows Controls],ITextDocument2 interface, ITextDocument2 interface [Windows Controls],GetDocumentPara method, ITextDocument2.GetDocumentPara, ITextDocument2::GetDocumentPara, controls.itextdocument2_getdocumentpara, tom/ITextDocument2::GetDocumentPara
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
 - ITextDocument2::GetDocumentPara
 - tom/ITextDocument2::GetDocumentPara
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
 - ITextDocument2.GetDocumentPara
---

# ITextDocument2::GetDocumentPara


## -description

Gets an object that provides the default paragraph format  information for this instance of the Text Object Model (TOM) engine.

## -parameters

### -param ppPara [out, retval]

Type: <b><a href="/windows/desktop/api/tom/nn-tom-itextpara2">ITextPara2</a>**</b>

The object that provides the default paragraph format  information.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextdocument2">ITextDocument2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextdocument2-setdocumentpara">ITextDocument2::SetDocumentPara</a>