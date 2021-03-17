---
UID: NF:tom.ITextPara2.SetHangingPunctuation
title: ITextPara2::SetHangingPunctuation (tom.h)
description: Sets whether to hang punctuation symbols on the right margin when the paragraph is justified.
helpviewer_keywords: ["ITextPara2 interface [Windows Controls]","SetHangingPunctuation method","ITextPara2.SetHangingPunctuation","ITextPara2::SetHangingPunctuation","SetHangingPunctuation","SetHangingPunctuation method [Windows Controls]","SetHangingPunctuation method [Windows Controls]","ITextPara2 interface","controls.itextpara2_sethangingpunctuation","tom/ITextPara2::SetHangingPunctuation"]
old-location: controls\itextpara2_sethangingpunctuation.htm
tech.root: Controls
ms.assetid: 8c70f76f-7a4a-49b3-bc16-8e90ad7ee041
ms.date: 12/05/2018
ms.keywords: ITextPara2 interface [Windows Controls],SetHangingPunctuation method, ITextPara2.SetHangingPunctuation, ITextPara2::SetHangingPunctuation, SetHangingPunctuation, SetHangingPunctuation method [Windows Controls], SetHangingPunctuation method [Windows Controls],ITextPara2 interface, controls.itextpara2_sethangingpunctuation, tom/ITextPara2::SetHangingPunctuation
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
 - ITextPara2::SetHangingPunctuation
 - tom/ITextPara2::SetHangingPunctuation
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
 - ITextPara2.SetHangingPunctuation
---

# ITextPara2::SetHangingPunctuation


## -description

Sets whether to hang
 punctuation symbols on the right margin when the paragraph is justified.

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
<td>Hang
 punctuation symbols on the right margin.</td>
</tr>
<tr>
<td><b>tomFalse</b></td>
<td>Do not hang
 punctuation symbols on the right margin.</td>
</tr>
<tr>
<td><b>tomToggle</b></td>
<td>Toggle the HangingPunctuation property.</td>
</tr>
<tr>
<td><b>tomUndefined</b></td>
<td>The HangingPunctuation property is undefined.</td>
</tr>
</table>

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextpara2">ITextPara2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextpara2-gethangingpunctuation">ITextPara2::GetHangingPunctuation</a>