---
UID: NF:tom.ITextFont2.GetAutospaceNumeric
title: ITextFont2::GetAutospaceNumeric (tom.h)
description: Gets the East Asian &quot;autospace numeric&quot; state.
helpviewer_keywords: ["GetAutospaceNumeric","GetAutospaceNumeric method [Windows Controls]","GetAutospaceNumeric method [Windows Controls]","ITextFont2 interface","ITextFont2 interface [Windows Controls]","GetAutospaceNumeric method","ITextFont2.GetAutospaceNumeric","ITextFont2::GetAutospaceNumeric","controls.itextfont2_getautospacenumeric","tom/ITextFont2::GetAutospaceNumeric"]
old-location: controls\itextfont2_getautospacenumeric.htm
tech.root: Controls
ms.assetid: 448a461b-779a-457e-8206-2055a73c9b45
ms.date: 12/05/2018
ms.keywords: GetAutospaceNumeric, GetAutospaceNumeric method [Windows Controls], GetAutospaceNumeric method [Windows Controls],ITextFont2 interface, ITextFont2 interface [Windows Controls],GetAutospaceNumeric method, ITextFont2.GetAutospaceNumeric, ITextFont2::GetAutospaceNumeric, controls.itextfont2_getautospacenumeric, tom/ITextFont2::GetAutospaceNumeric
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
 - ITextFont2::GetAutospaceNumeric
 - tom/ITextFont2::GetAutospaceNumeric
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
 - ITextFont2.GetAutospaceNumeric
---

# ITextFont2::GetAutospaceNumeric


## -description

Gets the East Asian "autospace numeric" state.

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
<td>Use East Asian autospace numerics.</td>
</tr>
<tr>
<td><b>tomFalse</b></td>
<td>Do not use East Asian autospace numerics.</td>
</tr>
<tr>
<td><b>tomUndefined</b></td>
<td>The AutospaceNumeric property is undefined.</td>
</tr>
</table>

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextfont2">ITextFont2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextfont2-setautospacenumeric">ITextFont2::SetAutospaceNumeric</a>