---
UID: NF:tom.ITextPara2.SetTrimPunctuationAtStart
title: ITextPara2::SetTrimPunctuationAtStart (tom.h)
description: Sets whether to trim the leading space of a punctuation symbol at the start of a line.
helpviewer_keywords: ["ITextPara2 interface [Windows Controls]","SetTrimPunctuationAtStart method","ITextPara2.SetTrimPunctuationAtStart","ITextPara2::SetTrimPunctuationAtStart","SetTrimPunctuationAtStart","SetTrimPunctuationAtStart method [Windows Controls]","SetTrimPunctuationAtStart method [Windows Controls]","ITextPara2 interface","controls.itextpara2_settrimpunctuationatstart","tom/ITextPara2::SetTrimPunctuationAtStart"]
old-location: controls\itextpara2_settrimpunctuationatstart.htm
tech.root: Controls
ms.assetid: f08f67ca-5767-4986-8af1-b3a11a1065aa
ms.date: 12/05/2018
ms.keywords: ITextPara2 interface [Windows Controls],SetTrimPunctuationAtStart method, ITextPara2.SetTrimPunctuationAtStart, ITextPara2::SetTrimPunctuationAtStart, SetTrimPunctuationAtStart, SetTrimPunctuationAtStart method [Windows Controls], SetTrimPunctuationAtStart method [Windows Controls],ITextPara2 interface, controls.itextpara2_settrimpunctuationatstart, tom/ITextPara2::SetTrimPunctuationAtStart
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
 - ITextPara2::SetTrimPunctuationAtStart
 - tom/ITextPara2::SetTrimPunctuationAtStart
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
 - ITextPara2.SetTrimPunctuationAtStart
---

# ITextPara2::SetTrimPunctuationAtStart


## -description

Sets whether to trim the leading space of a punctuation symbol at the start of a line.

## -parameters

### -param Value [in]

Type: <b>long</b>

A <a href="/windows/desktop/Controls/about-text-object-model">tomBool</a> that indicates whether to trim the leading space of a punctuation symbol. It can be one of the following values.

<table class="clsStd">
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td><b>tomTrue</b></td>
<td>Trim the leading space of a punctuation symbol at the start of a line.</td>
</tr>
<tr>
<td><b>tomFalse</b></td>
<td>Do not trim the leading space of a punctuation symbol at the start of a line.</td>
</tr>
<tr>
<td><b>tomToggle</b></td>
<td>Toggle the TrimPunctuationAtStart property.</td>
</tr>
<tr>
<td><b>tomUndefined</b></td>
<td>The TrimPunctuationAtStart property is undefined.</td>
</tr>
</table>

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextpara2">ITextPara2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextpara2-gettrimpunctuationatstart">ITextPara2::GetTrimPunctuationAtStart</a>