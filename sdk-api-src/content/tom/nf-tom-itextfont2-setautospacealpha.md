---
UID: NF:tom.ITextFont2.SetAutospaceAlpha
title: ITextFont2::SetAutospaceAlpha (tom.h)
description: Sets the East Asian &quot;autospace alpha&quot; state.
helpviewer_keywords: ["ITextFont2 interface [Windows Controls]","SetAutospaceAlpha method","ITextFont2.SetAutospaceAlpha","ITextFont2::SetAutospaceAlpha","SetAutospaceAlpha","SetAutospaceAlpha method [Windows Controls]","SetAutospaceAlpha method [Windows Controls]","ITextFont2 interface","controls.itextfont2_setautospacealpha","tom/ITextFont2::SetAutospaceAlpha"]
old-location: controls\itextfont2_setautospacealpha.htm
tech.root: Controls
ms.assetid: 8a01677d-74c6-437b-8ee9-350c891c6c3f
ms.date: 12/05/2018
ms.keywords: ITextFont2 interface [Windows Controls],SetAutospaceAlpha method, ITextFont2.SetAutospaceAlpha, ITextFont2::SetAutospaceAlpha, SetAutospaceAlpha, SetAutospaceAlpha method [Windows Controls], SetAutospaceAlpha method [Windows Controls],ITextFont2 interface, controls.itextfont2_setautospacealpha, tom/ITextFont2::SetAutospaceAlpha
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
 - ITextFont2::SetAutospaceAlpha
 - tom/ITextFont2::SetAutospaceAlpha
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
 - ITextFont2.SetAutospaceAlpha
---

# ITextFont2::SetAutospaceAlpha


## -description

Sets the East Asian "autospace alpha" state.

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
<td>Use East Asian autospace alphabetics.</td>
</tr>
<tr>
<td><b>tomFalse</b></td>
<td>Do not use East Asian autospace alphabetics.</td>
</tr>
<tr>
<td><b>tomToggle</b></td>
<td>Toggle the AutospaceAlpha property.</td>
</tr>
<tr>
<td><b>tomUndefined</b></td>
<td>The AutospaceAlpha property is undefined.</td>
</tr>
</table>

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextfont2">ITextFont2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextfont2-getautospacealpha">ITextFont2::GetAutospaceAlpha</a>