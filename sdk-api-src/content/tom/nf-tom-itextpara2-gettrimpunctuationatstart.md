---
UID: NF:tom.ITextPara2.GetTrimPunctuationAtStart
title: ITextPara2::GetTrimPunctuationAtStart (tom.h)
description: Gets whether to trim the leading space of a punctuation symbol at the start of a line.
helpviewer_keywords: ["GetTrimPunctuationAtStart","GetTrimPunctuationAtStart method [Windows Controls]","GetTrimPunctuationAtStart method [Windows Controls]","ITextPara2 interface","ITextPara2 interface [Windows Controls]","GetTrimPunctuationAtStart method","ITextPara2.GetTrimPunctuationAtStart","ITextPara2::GetTrimPunctuationAtStart","controls.itextpara2_gettrimpunctuationatstart","tom/ITextPara2::GetTrimPunctuationAtStart"]
old-location: controls\itextpara2_gettrimpunctuationatstart.htm
tech.root: Controls
ms.assetid: 965df0ef-b8ff-4d0e-8124-c811e74e0208
ms.date: 12/05/2018
ms.keywords: GetTrimPunctuationAtStart, GetTrimPunctuationAtStart method [Windows Controls], GetTrimPunctuationAtStart method [Windows Controls],ITextPara2 interface, ITextPara2 interface [Windows Controls],GetTrimPunctuationAtStart method, ITextPara2.GetTrimPunctuationAtStart, ITextPara2::GetTrimPunctuationAtStart, controls.itextpara2_gettrimpunctuationatstart, tom/ITextPara2::GetTrimPunctuationAtStart
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
 - ITextPara2::GetTrimPunctuationAtStart
 - tom/ITextPara2::GetTrimPunctuationAtStart
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
 - ITextPara2.GetTrimPunctuationAtStart
---

# ITextPara2::GetTrimPunctuationAtStart


## -description

Gets whether to trim the leading space of a punctuation symbol at the start of a line.

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
<td>Trim the leading space of a punctuation symbol at the start of a line.</td>
</tr>
<tr>
<td><b>tomFalse</b></td>
<td>Do not trim the leading space of a punctuation symbol at the start of a line.</td>
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



<a href="/windows/desktop/api/tom/nf-tom-itextpara2-settrimpunctuationatstart">ITextPara2::SetTrimPunctuationAtStart</a>