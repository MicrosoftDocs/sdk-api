---
UID: NF:tom.ITextFont2.SetModWidthSpace
title: ITextFont2::SetModWidthSpace (tom.h)
description: Sets whether &quot;increase width of whitespace&quot; is active.
helpviewer_keywords: ["ITextFont2 interface [Windows Controls]","SetModWidthSpace method","ITextFont2.SetModWidthSpace","ITextFont2::SetModWidthSpace","SetModWidthSpace","SetModWidthSpace method [Windows Controls]","SetModWidthSpace method [Windows Controls]","ITextFont2 interface","controls.itextfont2_setmodwidthspace","tom/ITextFont2::SetModWidthSpace"]
old-location: controls\itextfont2_setmodwidthspace.htm
tech.root: Controls
ms.assetid: df3ea127-1f47-4173-ad2c-0a7af4c8454c
ms.date: 12/05/2018
ms.keywords: ITextFont2 interface [Windows Controls],SetModWidthSpace method, ITextFont2.SetModWidthSpace, ITextFont2::SetModWidthSpace, SetModWidthSpace, SetModWidthSpace method [Windows Controls], SetModWidthSpace method [Windows Controls],ITextFont2 interface, controls.itextfont2_setmodwidthspace, tom/ITextFont2::SetModWidthSpace
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
 - ITextFont2::SetModWidthSpace
 - tom/ITextFont2::SetModWidthSpace
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
 - ITextFont2.SetModWidthSpace
---

# ITextFont2::SetModWidthSpace


## -description

Sets whether "increase width of whitespace" is active.

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
<td>Increase width of whitespace is active.</td>
</tr>
<tr>
<td><b>tomFalse</b></td>
<td>Increase width of whitespace is not active.</td>
</tr>
<tr>
<td><b>tomToggle</b></td>
<td>Toggle the ModWidthSpace property.</td>
</tr>
<tr>
<td><b>tomUndefined</b></td>
<td>The ModWidthSpace property is undefined.</td>
</tr>
</table>

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextfont2">ITextFont2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextfont2-getmodwidthspace">ITextFont2::GetModWidthSpace</a>