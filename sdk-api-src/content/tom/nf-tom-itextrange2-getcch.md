---
UID: NF:tom.ITextRange2.GetCch
title: ITextRange2::GetCch (tom.h)
description: Gets the count of characters in a range.
helpviewer_keywords: ["GetCch","GetCch method [Windows Controls]","GetCch method [Windows Controls]","ITextRange2 interface","ITextRange2 interface [Windows Controls]","GetCch method","ITextRange2.GetCch","ITextRange2::GetCch","controls.itextrange2_getcch","tom/ITextRange2::GetCch"]
old-location: controls\itextrange2_getcch.htm
tech.root: Controls
ms.assetid: a6f06062-3c8f-40c0-9b5d-6c22a647bfbc
ms.date: 12/05/2018
ms.keywords: GetCch, GetCch method [Windows Controls], GetCch method [Windows Controls],ITextRange2 interface, ITextRange2 interface [Windows Controls],GetCch method, ITextRange2.GetCch, ITextRange2::GetCch, controls.itextrange2_getcch, tom/ITextRange2::GetCch
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
 - ITextRange2::GetCch
 - tom/ITextRange2::GetCch
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
 - ITextRange2.GetCch
---

# ITextRange2::GetCch


## -description

Gets the count of characters in a range.

## -parameters

### -param pcch [out, retval]

Type: <b>long*</b>

The signed count of characters.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The count of characters is the difference between the character position of the active end of the range, and the character position of the anchor end. Some Text Object Model (TOM) implementations might include active ends only for a selection (represented by the <a href="/windows/desktop/api/tom/nn-tom-itextselection">ITextSelection</a> interface). The rich edit control's TOM implementation of a text range (represented by the <a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a> interface) also has active ends.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a>