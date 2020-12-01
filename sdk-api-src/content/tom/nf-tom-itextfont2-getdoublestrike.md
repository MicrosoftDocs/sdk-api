---
UID: NF:tom.ITextFont2.GetDoubleStrike
title: ITextFont2::GetDoubleStrike (tom.h)
description: Gets whether characters are displayed with double horizontal lines through the center.
helpviewer_keywords: ["GetDoubleStrike","GetDoubleStrike method [Windows Controls]","GetDoubleStrike method [Windows Controls]","ITextFont2 interface","ITextFont2 interface [Windows Controls]","GetDoubleStrike method","ITextFont2.GetDoubleStrike","ITextFont2::GetDoubleStrike","controls.itextfont2_getdoublestrike","tom/ITextFont2::GetDoubleStrike"]
old-location: controls\itextfont2_getdoublestrike.htm
tech.root: Controls
ms.assetid: 9e599c29-4b47-4043-b9c7-75a736ca64fa
ms.date: 12/05/2018
ms.keywords: GetDoubleStrike, GetDoubleStrike method [Windows Controls], GetDoubleStrike method [Windows Controls],ITextFont2 interface, ITextFont2 interface [Windows Controls],GetDoubleStrike method, ITextFont2.GetDoubleStrike, ITextFont2::GetDoubleStrike, controls.itextfont2_getdoublestrike, tom/ITextFont2::GetDoubleStrike
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
 - ITextFont2::GetDoubleStrike
 - tom/ITextFont2::GetDoubleStrike
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
 - ITextFont2.GetDoubleStrike
---

# ITextFont2::GetDoubleStrike


## -description

Gets whether characters are displayed with double horizontal lines through the center.

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
<td>Characters are displayed with double horizontal lines.</td>
</tr>
<tr>
<td><b>tomFalse</b></td>
<td>Characters are not displayed with double horizontal lines.</td>
</tr>
<tr>
<td><b>tomUndefined</b></td>
<td>The DoubleStrike property is undefined.</td>
</tr>
</table>

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextfont2">ITextFont2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextfont2-setdoublestrike">ITextFont2::SetDoubleStrike</a>