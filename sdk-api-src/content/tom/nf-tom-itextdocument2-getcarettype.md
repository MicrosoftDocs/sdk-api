---
UID: NF:tom.ITextDocument2.GetCaretType
title: ITextDocument2::GetCaretType (tom.h)
description: Gets the caret type.
helpviewer_keywords: ["GetCaretType","GetCaretType method [Windows Controls]","GetCaretType method [Windows Controls]","ITextDocument2 interface","ITextDocument2 interface [Windows Controls]","GetCaretType method","ITextDocument2.GetCaretType","ITextDocument2::GetCaretType","controls.itextdocument2_getcarettype","tom/ITextDocument2::GetCaretType","tomKoreanBlockCaret","tomNormalCaret","tomNullCaret"]
old-location: controls\itextdocument2_getcarettype.htm
tech.root: Controls
ms.assetid: 4ab170d2-50a3-4fbf-8e02-92b031bc1e4f
ms.date: 12/05/2018
ms.keywords: GetCaretType, GetCaretType method [Windows Controls], GetCaretType method [Windows Controls],ITextDocument2 interface, ITextDocument2 interface [Windows Controls],GetCaretType method, ITextDocument2.GetCaretType, ITextDocument2::GetCaretType, controls.itextdocument2_getcarettype, tom/ITextDocument2::GetCaretType, tomKoreanBlockCaret, tomNormalCaret, tomNullCaret
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
 - ITextDocument2::GetCaretType
 - tom/ITextDocument2::GetCaretType
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
 - ITextDocument2.GetCaretType
---

# ITextDocument2::GetCaretType


## -description

Gets the caret type.

## -parameters

### -param pValue [out, retval]

Type: <b>long*</b>

The caret type. It can be one of the following values:

<a id="tomKoreanBlockCaret"></a>
<a id="tomkoreanblockcaret"></a>
<a id="TOMKOREANBLOCKCARET"></a>


#### tomKoreanBlockCaret

<a id="tomNormalCaret"></a>
<a id="tomnormalcaret"></a>
<a id="TOMNORMALCARET"></a>


#### tomNormalCaret

<a id="tomNullCaret"></a>
<a id="tomnullcaret"></a>
<a id="TOMNULLCARET"></a>


#### tomNullCaret

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextdocument2">ITextDocument2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextdocument2-setcarettype">ITextDocument2::SetCaretType</a>