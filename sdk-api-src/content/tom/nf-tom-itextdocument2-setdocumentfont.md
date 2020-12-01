---
UID: NF:tom.ITextDocument2.SetDocumentFont
title: ITextDocument2::SetDocumentFont (tom.h)
description: Sets the default character formatting for this instance of the Text Object Model (TOM) engine.
helpviewer_keywords: ["ITextDocument2 interface [Windows Controls]","SetDocumentFont method","ITextDocument2.SetDocumentFont","ITextDocument2::SetDocumentFont","SetDocumentFont","SetDocumentFont method [Windows Controls]","SetDocumentFont method [Windows Controls]","ITextDocument2 interface","controls.itextdocument2_setdocumentfont","tom/ITextDocument2::SetDocumentFont"]
old-location: controls\itextdocument2_setdocumentfont.htm
tech.root: Controls
ms.assetid: 1fbc000a-76c2-4b80-856b-42f2e1829e93
ms.date: 12/05/2018
ms.keywords: ITextDocument2 interface [Windows Controls],SetDocumentFont method, ITextDocument2.SetDocumentFont, ITextDocument2::SetDocumentFont, SetDocumentFont, SetDocumentFont method [Windows Controls], SetDocumentFont method [Windows Controls],ITextDocument2 interface, controls.itextdocument2_setdocumentfont, tom/ITextDocument2::SetDocumentFont
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
 - ITextDocument2::SetDocumentFont
 - tom/ITextDocument2::SetDocumentFont
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
 - ITextDocument2.SetDocumentFont
---

# ITextDocument2::SetDocumentFont


## -description

Sets  the default character formatting for this instance of the Text Object Model (TOM) engine.

## -parameters

### -param pFont [in]

Type: <b><a href="/windows/desktop/api/tom/nn-tom-itextfont2">ITextFont2</a>*</b>

The font object that provides the default character formatting.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

You can also set the default character formatting by calling <a href="/windows/desktop/api/tom/nf-tom-itextfont-reset">ITextFont::Reset(tomDefault)</a>.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextdocument2">ITextDocument2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextdocument2-getdocumentfont">ITextDocument2::GetDocumentFont</a>



<a href="/windows/desktop/api/tom/nf-tom-itextfont-reset">ITextFont::Reset</a>