---
UID: NF:tom.ITextStrings.EncodeFunction
title: ITextStrings::EncodeFunction (tom.h)
description: Encodes an object, given a set of argument strings.
helpviewer_keywords: ["EncodeFunction","EncodeFunction method [Windows Controls]","EncodeFunction method [Windows Controls]","ITextStrings interface","ITextStrings interface [Windows Controls]","EncodeFunction method","ITextStrings.EncodeFunction","ITextStrings::EncodeFunction","controls.itextstrings_encodefunction","tom/ITextStrings::EncodeFunction"]
old-location: controls\itextstrings_encodefunction.htm
tech.root: Controls
ms.assetid: f22bb343-4fcc-4473-84cc-807011b5a7b0
ms.date: 12/05/2018
ms.keywords: EncodeFunction, EncodeFunction method [Windows Controls], EncodeFunction method [Windows Controls],ITextStrings interface, ITextStrings interface [Windows Controls],EncodeFunction method, ITextStrings.EncodeFunction, ITextStrings::EncodeFunction, controls.itextstrings_encodefunction, tom/ITextStrings::EncodeFunction
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
 - ITextStrings::EncodeFunction
 - tom/ITextStrings::EncodeFunction
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
 - ITextStrings.EncodeFunction
---

# ITextStrings::EncodeFunction


## -description

Encodes an object, given a set of argument strings.

## -parameters

### -param Type [in]

Type: <b>long</b>

The object type. See <a href="/windows/desktop/api/tom/nf-tom-itextrange2-getinlineobject">ITextRange2::GetInlineObject</a> for a table of definitions.

### -param Align [in]

Type: <b>long</b>

The object alignment. See <a href="/windows/desktop/api/tom/nf-tom-itextrange2-getinlineobject">ITextRange2::GetInlineObject</a> for a table of definitions.

### -param Char [in]

Type: <b>long</b>

The object character.

### -param Char1 [in]

Type: <b>long</b>

The object character.

### -param Char2 [in]

Type: <b>long</b>

The object character.

### -param Count [in]

Type: <b>long</b>

The count of strings (arguments) to concatenate.

### -param TeXStyle [in]

Type: <b>long</b>

The TeX style.

### -param cCol [in]

Type: <b>long</b>

The count of columns (<b>tomArray</b> only).

### -param pRange [in]

Type: <b><a href="/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a>*</b>

The specifying range that points at the desired formatting.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

See <a href="/windows/desktop/api/tom/nf-tom-itextrange2-getinlineobject">ITextRange2::GetInlineObject</a> for a more detailed discussion of the arguments.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextstrings">ITextStrings</a>