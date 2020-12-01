---
UID: NF:tom.ITextFont2.GetAutospaceParens
title: ITextFont2::GetAutospaceParens (tom.h)
description: Gets the East Asian &quot;autospace parentheses&quot; state.
helpviewer_keywords: ["GetAutospaceParens","GetAutospaceParens method [Windows Controls]","GetAutospaceParens method [Windows Controls]","ITextFont2 interface","ITextFont2 interface [Windows Controls]","GetAutospaceParens method","ITextFont2.GetAutospaceParens","ITextFont2::GetAutospaceParens","controls.itextfont2_getautospaceparens","tom/ITextFont2::GetAutospaceParens"]
old-location: controls\itextfont2_getautospaceparens.htm
tech.root: Controls
ms.assetid: fce60349-cded-4cab-b2e5-4fad02d11195
ms.date: 12/05/2018
ms.keywords: GetAutospaceParens, GetAutospaceParens method [Windows Controls], GetAutospaceParens method [Windows Controls],ITextFont2 interface, ITextFont2 interface [Windows Controls],GetAutospaceParens method, ITextFont2.GetAutospaceParens, ITextFont2::GetAutospaceParens, controls.itextfont2_getautospaceparens, tom/ITextFont2::GetAutospaceParens
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
 - ITextFont2::GetAutospaceParens
 - tom/ITextFont2::GetAutospaceParens
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
 - ITextFont2.GetAutospaceParens
---

# ITextFont2::GetAutospaceParens


## -description

Gets the East Asian "autospace parentheses" state.

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
<td>Use East Asian autospace parentheses.</td>
</tr>
<tr>
<td><b>tomFalse</b></td>
<td>Do not use East Asian autospace parentheses.</td>
</tr>
<tr>
<td><b>tomUndefined</b></td>
<td>The AutospaceParens property is undefined.</td>
</tr>
</table>

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextfont2">ITextFont2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextfont2-setautospaceparens">ITextFont2::SetAutospaceParens</a>