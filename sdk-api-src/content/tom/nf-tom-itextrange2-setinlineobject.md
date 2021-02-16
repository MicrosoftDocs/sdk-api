---
UID: NF:tom.ITextRange2.SetInlineObject
title: ITextRange2::SetInlineObject (tom.h)
description: Sets or inserts the properties of an inline object for a degenerate range.
helpviewer_keywords: ["ITextRange2 interface [Windows Controls]","SetInlineObject method","ITextRange2.SetInlineObject","ITextRange2::SetInlineObject","SetInlineObject","SetInlineObject method [Windows Controls]","SetInlineObject method [Windows Controls]","ITextRange2 interface","controls.itextrange2_setinlineobject","tom/ITextRange2::SetInlineObject"]
old-location: controls\itextrange2_setinlineobject.htm
tech.root: Controls
ms.assetid: 56876a42-a972-4a19-a8f7-a5e37c0d77f0
ms.date: 12/05/2018
ms.keywords: ITextRange2 interface [Windows Controls],SetInlineObject method, ITextRange2.SetInlineObject, ITextRange2::SetInlineObject, SetInlineObject, SetInlineObject method [Windows Controls], SetInlineObject method [Windows Controls],ITextRange2 interface, controls.itextrange2_setinlineobject, tom/ITextRange2::SetInlineObject
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
 - ITextRange2::SetInlineObject
 - tom/ITextRange2::SetInlineObject
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
 - ITextRange2.SetInlineObject
---

# ITextRange2::SetInlineObject


## -description

Sets or inserts the properties of an inline object for a degenerate range.

## -parameters

### -param Type [in]

Type: <b>long</b>

The object type as defined in <a href="/windows/desktop/api/tom/nf-tom-itextrange2-getinlineobject">ITextRange2::GetInlineObject</a>.

### -param Align [in]

Type: <b>long</b>

The object alignment as defined in <a href="/windows/desktop/api/tom/nf-tom-itextrange2-getinlineobject">ITextRange2::GetInlineObject</a>.

### -param Char [in]

Type: <b>long</b>

The object character as defined in <a href="/windows/desktop/api/tom/nf-tom-itextrange2-getinlineobject">ITextRange2::GetInlineObject</a>.

### -param Char1 [in]

Type: <b>long</b>

The closing bracket (<a href="/windows/win32/api/tom/ne-tom-objecttype">tomBrackets</a>) character. See <a href="https://www.unicode.org/notes/tn28/">Unicode Technical Note 28</a> for a list of characters.

### -param Char2 [in]

Type: <b>long</b>

The separator character for <a href="/windows/win32/api/tom/ne-tom-objecttype">tomBracketsWithSeps</a>, which can be one of the following values.

### -param Count [in]

Type: <b>long</b>

The number of arguments in the inline object.

### -param TeXStyle [in]

Type: <b>long</b>

The TeX style, as defined in <a href="/windows/desktop/api/tom/nf-tom-itextrange2-getinlineobject">ITextRange2::GetInlineObject</a>.

### -param cCol [in]

Type: <b>long</b>

The number of columns in the inline object. For  <a href="/windows/win32/api/tom/ne-tom-objecttype">tomMatrix</a> only.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrange2-getinlineobject">ITextRange2::GetInlineObject</a>