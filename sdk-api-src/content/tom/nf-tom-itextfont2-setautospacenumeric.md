---
UID: NF:tom.ITextFont2.SetAutospaceNumeric
title: ITextFont2::SetAutospaceNumeric (tom.h)
description: Sets the East Asian &quot;autospace numeric&quot; state.
helpviewer_keywords: ["ITextFont2 interface [Windows Controls]","SetAutospaceNumeric method","ITextFont2.SetAutospaceNumeric","ITextFont2::SetAutospaceNumeric","SetAutospaceNumeric","SetAutospaceNumeric method [Windows Controls]","SetAutospaceNumeric method [Windows Controls]","ITextFont2 interface","controls.itextfont2_setautospacenumeric","tom/ITextFont2::SetAutospaceNumeric"]
old-location: controls\itextfont2_setautospacenumeric.htm
tech.root: Controls
ms.assetid: 7fd911c2-a765-4bbc-a14c-15665d5a4a16
ms.date: 12/05/2018
ms.keywords: ITextFont2 interface [Windows Controls],SetAutospaceNumeric method, ITextFont2.SetAutospaceNumeric, ITextFont2::SetAutospaceNumeric, SetAutospaceNumeric, SetAutospaceNumeric method [Windows Controls], SetAutospaceNumeric method [Windows Controls],ITextFont2 interface, controls.itextfont2_setautospacenumeric, tom/ITextFont2::SetAutospaceNumeric
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
 - ITextFont2::SetAutospaceNumeric
 - tom/ITextFont2::SetAutospaceNumeric
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
 - ITextFont2.SetAutospaceNumeric
---

# ITextFont2::SetAutospaceNumeric


## -description

Sets the East Asian "autospace numeric" state.

## -parameters

### -param Value [in]

Type: <b>long</b>

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
<td><b>tomToggle</b></td>
<td>Toggle the AutospaceNumeric property.</td>
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



<a href="/windows/desktop/api/tom/nf-tom-itextfont2-getautospacenumeric">ITextFont2::GetAutospaceNumeric</a>