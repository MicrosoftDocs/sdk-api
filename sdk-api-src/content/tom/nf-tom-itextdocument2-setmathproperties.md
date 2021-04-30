---
UID: NF:tom.ITextDocument2.SetMathProperties
title: ITextDocument2::SetMathProperties (tom.h)
description: Specifies the math properties to use for the document.
helpviewer_keywords: ["ITextDocument2 interface [Windows Controls]","SetMathProperties method","ITextDocument2.SetMathProperties","ITextDocument2::SetMathProperties","SetMathProperties","SetMathProperties method [Windows Controls]","SetMathProperties method [Windows Controls]","ITextDocument2 interface","controls.itextdocument2_setmathproperties","tom/ITextDocument2::SetMathProperties"]
old-location: controls\itextdocument2_setmathproperties.htm
tech.root: Controls
ms.assetid: a688354b-b231-44fc-9cfb-32c8e8b1361f
ms.date: 12/05/2018
ms.keywords: ITextDocument2 interface [Windows Controls],SetMathProperties method, ITextDocument2.SetMathProperties, ITextDocument2::SetMathProperties, SetMathProperties, SetMathProperties method [Windows Controls], SetMathProperties method [Windows Controls],ITextDocument2 interface, controls.itextdocument2_setmathproperties, tom/ITextDocument2::SetMathProperties
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
 - ITextDocument2::SetMathProperties
 - tom/ITextDocument2::SetMathProperties
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
 - ITextDocument2.SetMathProperties
---

# ITextDocument2::SetMathProperties


## -description

Specifies the math properties to use for the document.

## -parameters

### -param Options [in]

Type: <b>long</b>

The math properties to set. For a list of possible properties, see <a href="/windows/desktop/api/tom/nf-tom-itextdocument2-getmathproperties">GetMathProperties</a>.

### -param Mask [in]

Type: <b>long</b>

The math mask. For a list of possible masks, see <a href="/windows/desktop/api/tom/nf-tom-itextdocument2-getmathproperties">GetMathProperties</a>

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextdocument2">ITextDocument2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextdocument2-getmathproperties">ITextDocument2::GetMathProperties</a>