---
UID: NF:tom.ITextDocument2.SetDocumentPara
title: ITextDocument2::SetDocumentPara (tom.h)
description: Sets the default paragraph formatting for this instance of the Text Object Model (TOM) engine.
helpviewer_keywords: ["ITextDocument2 interface [Windows Controls]","SetDocumentPara method","ITextDocument2.SetDocumentPara","ITextDocument2::SetDocumentPara","SetDocumentPara","SetDocumentPara method [Windows Controls]","SetDocumentPara method [Windows Controls]","ITextDocument2 interface","controls.itextdocument2_setdocumentpara","tom/ITextDocument2::SetDocumentPara"]
old-location: controls\itextdocument2_setdocumentpara.htm
tech.root: Controls
ms.assetid: d35d57e9-a005-48cd-a92d-381dc490d44f
ms.date: 12/05/2018
ms.keywords: ITextDocument2 interface [Windows Controls],SetDocumentPara method, ITextDocument2.SetDocumentPara, ITextDocument2::SetDocumentPara, SetDocumentPara, SetDocumentPara method [Windows Controls], SetDocumentPara method [Windows Controls],ITextDocument2 interface, controls.itextdocument2_setdocumentpara, tom/ITextDocument2::SetDocumentPara
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
 - ITextDocument2::SetDocumentPara
 - tom/ITextDocument2::SetDocumentPara
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
 - ITextDocument2.SetDocumentPara
---

# ITextDocument2::SetDocumentPara


## -description

Sets the default paragraph formatting  for this instance of the Text Object Model (TOM) engine.

## -parameters

### -param pPara [in]

Type: <b><a href="/windows/desktop/api/tom/nn-tom-itextpara2">ITextPara2</a>*</b>

The paragraph object that provides the default paragraph formatting

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

You can also set the default paragraph formatting by calling <a href="/windows/desktop/api/tom/nf-tom-itextpara-reset">ITextPara::Reset(tomDefault)</a>.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextdocument2">ITextDocument2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextdocument2-getdocumentpara">ITextDocument2::GetDocumentPara</a>