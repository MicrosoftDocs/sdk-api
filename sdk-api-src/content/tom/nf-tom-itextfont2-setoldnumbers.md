---
UID: NF:tom.ITextFont2.SetOldNumbers
title: ITextFont2::SetOldNumbers (tom.h)
description: Sets whether old-style numbers are active.
helpviewer_keywords: ["ITextFont2 interface [Windows Controls]","SetOldNumbers method","ITextFont2.SetOldNumbers","ITextFont2::SetOldNumbers","SetOldNumbers","SetOldNumbers method [Windows Controls]","SetOldNumbers method [Windows Controls]","ITextFont2 interface","controls.itextfont2_setoldnumbers","tom/ITextFont2::SetOldNumbers"]
old-location: controls\itextfont2_setoldnumbers.htm
tech.root: Controls
ms.assetid: f510781e-ede9-41dc-ae69-3b0ca52a6773
ms.date: 12/05/2018
ms.keywords: ITextFont2 interface [Windows Controls],SetOldNumbers method, ITextFont2.SetOldNumbers, ITextFont2::SetOldNumbers, SetOldNumbers, SetOldNumbers method [Windows Controls], SetOldNumbers method [Windows Controls],ITextFont2 interface, controls.itextfont2_setoldnumbers, tom/ITextFont2::SetOldNumbers
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
 - ITextFont2::SetOldNumbers
 - tom/ITextFont2::SetOldNumbers
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
 - ITextFont2.SetOldNumbers
---

# ITextFont2::SetOldNumbers


## -description

Sets whether old-style numbers are active.

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
<td>Old-style numbers are active.</td>
</tr>
<tr>
<td><b>tomFalse</b></td>
<td>Old-style numbers are not active.</td>
</tr>
<tr>
<td><b>tomToggle</b></td>
<td>Toggle the OldNumbers property.</td>
</tr>
<tr>
<td><b>tomUndefined</b></td>
<td>The OldNumbers property is undefined.</td>
</tr>
</table>

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextfont2">ITextFont2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextfont2-getoldnumbers">ITextFont2::GetOldNumbers</a>