---
UID: NF:tom.ITextDocument2.SetCaretType
title: ITextDocument2::SetCaretType (tom.h)
description: Sets the caret type.
helpviewer_keywords: ["ITextDocument2 interface [Windows Controls]","SetCaretType method","ITextDocument2.SetCaretType","ITextDocument2::SetCaretType","SetCaretType","SetCaretType method [Windows Controls]","SetCaretType method [Windows Controls]","ITextDocument2 interface","controls.itextdocument2_setcarettype","tom/ITextDocument2::SetCaretType","tomKoreanBlockCaret","tomNormalCaret","tomNullCaret"]
old-location: controls\itextdocument2_setcarettype.htm
tech.root: Controls
ms.assetid: 40d34482-cf07-4401-ad02-f5d1b0184976
ms.date: 12/05/2018
ms.keywords: ITextDocument2 interface [Windows Controls],SetCaretType method, ITextDocument2.SetCaretType, ITextDocument2::SetCaretType, SetCaretType, SetCaretType method [Windows Controls], SetCaretType method [Windows Controls],ITextDocument2 interface, controls.itextdocument2_setcarettype, tom/ITextDocument2::SetCaretType, tomKoreanBlockCaret, tomNormalCaret, tomNullCaret
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
 - ITextDocument2::SetCaretType
 - tom/ITextDocument2::SetCaretType
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
 - ITextDocument2.SetCaretType
---

# ITextDocument2::SetCaretType


## -description

Sets the caret type.

## -parameters

### -param Value [in]

Type: <b>long</b>

The new caret type. It can be one of the following values:

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



<a href="/windows/desktop/api/tom/nf-tom-itextdocument2-getcarettype">ITextDocument2::GetCaretType</a>