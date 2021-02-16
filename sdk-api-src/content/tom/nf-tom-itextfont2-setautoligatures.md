---
UID: NF:tom.ITextFont2.SetAutoLigatures
title: ITextFont2::SetAutoLigatures (tom.h)
description: Sets whether support for automatic ligatures is active.
helpviewer_keywords: ["ITextFont2 interface [Windows Controls]","SetAutoLigatures method","ITextFont2.SetAutoLigatures","ITextFont2::SetAutoLigatures","SetAutoLigatures","SetAutoLigatures method [Windows Controls]","SetAutoLigatures method [Windows Controls]","ITextFont2 interface","controls.itextfont2_setautoligatures","tom/ITextFont2::SetAutoLigatures"]
old-location: controls\itextfont2_setautoligatures.htm
tech.root: Controls
ms.assetid: f40fecfe-3c3b-46f0-9edf-ba48236e50e7
ms.date: 12/05/2018
ms.keywords: ITextFont2 interface [Windows Controls],SetAutoLigatures method, ITextFont2.SetAutoLigatures, ITextFont2::SetAutoLigatures, SetAutoLigatures, SetAutoLigatures method [Windows Controls], SetAutoLigatures method [Windows Controls],ITextFont2 interface, controls.itextfont2_setautoligatures, tom/ITextFont2::SetAutoLigatures
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
 - ITextFont2::SetAutoLigatures
 - tom/ITextFont2::SetAutoLigatures
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
 - ITextFont2.SetAutoLigatures
---

# ITextFont2::SetAutoLigatures


## -description

Sets whether support for automatic ligatures is active.

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
<td>Automatic ligature support is active.</td>
</tr>
<tr>
<td><b>tomFalse</b></td>
<td>Automatic ligature support is not active.</td>
</tr>
<tr>
<td><b>tomToggle</b></td>
<td>Toggle the AutoLigatures property.</td>
</tr>
<tr>
<td><b>tomUndefined</b></td>
<td>The AutoLigatures property is undefined.</td>
</tr>
</table>

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextfont2">ITextFont2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextfont2-getautoligatures">ITextFont2::GetAutoLigatures</a>