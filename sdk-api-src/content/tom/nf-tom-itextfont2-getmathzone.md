---
UID: NF:tom.ITextFont2.GetMathZone
title: ITextFont2::GetMathZone (tom.h)
description: Gets whether a math zone is active.
helpviewer_keywords: ["GetMathZone","GetMathZone method [Windows Controls]","GetMathZone method [Windows Controls]","ITextFont2 interface","ITextFont2 interface [Windows Controls]","GetMathZone method","ITextFont2.GetMathZone","ITextFont2::GetMathZone","controls.itextfont2_getmathzone","tom/ITextFont2::GetMathZone"]
old-location: controls\itextfont2_getmathzone.htm
tech.root: Controls
ms.assetid: 4da4d6d1-16e0-4891-9a60-c1330345e45a
ms.date: 12/05/2018
ms.keywords: GetMathZone, GetMathZone method [Windows Controls], GetMathZone method [Windows Controls],ITextFont2 interface, ITextFont2 interface [Windows Controls],GetMathZone method, ITextFont2.GetMathZone, ITextFont2::GetMathZone, controls.itextfont2_getmathzone, tom/ITextFont2::GetMathZone
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
 - ITextFont2::GetMathZone
 - tom/ITextFont2::GetMathZone
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
 - ITextFont2.GetMathZone
---

# ITextFont2::GetMathZone


## -description

Gets whether a math zone is active.

## -parameters

### -param pValue [out, retval]

Type: <b>long*</b>

A <a href="/windows/desktop/Controls/about-text-object-model">tomBool</a> value that can be one of the following.

<table class="clsStd">
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td><b>tomTrue</b></td>
<td>A math zone is active.</td>
</tr>
<tr>
<td><b>tomFalse</b></td>
<td>A math zone is not active.</td>
</tr>
<tr>
<td><b>tomUndefined</b></td>
<td>The MathZone property is undefined.</td>
</tr>
</table>

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextfont2">ITextFont2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextfont2-setmathzone">ITextFont2::SetMathZone</a>