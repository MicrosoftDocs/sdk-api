---
UID: NF:tom.ITextFont2.GetModWidthPairs
title: ITextFont2::GetModWidthPairs (tom.h)
description: Gets whether &quot;decrease widths on pairs&quot; is active.
helpviewer_keywords: ["GetModWidthPairs","GetModWidthPairs method [Windows Controls]","GetModWidthPairs method [Windows Controls]","ITextFont2 interface","ITextFont2 interface [Windows Controls]","GetModWidthPairs method","ITextFont2.GetModWidthPairs","ITextFont2::GetModWidthPairs","controls.itextfont2_getmodwidthpairs","tom/ITextFont2::GetModWidthPairs"]
old-location: controls\itextfont2_getmodwidthpairs.htm
tech.root: Controls
ms.assetid: 8fcbc781-42da-46aa-b231-3a8246eccd36
ms.date: 12/05/2018
ms.keywords: GetModWidthPairs, GetModWidthPairs method [Windows Controls], GetModWidthPairs method [Windows Controls],ITextFont2 interface, ITextFont2 interface [Windows Controls],GetModWidthPairs method, ITextFont2.GetModWidthPairs, ITextFont2::GetModWidthPairs, controls.itextfont2_getmodwidthpairs, tom/ITextFont2::GetModWidthPairs
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
 - ITextFont2::GetModWidthPairs
 - tom/ITextFont2::GetModWidthPairs
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
 - ITextFont2.GetModWidthPairs
---

# ITextFont2::GetModWidthPairs


## -description

Gets whether "decrease widths on pairs" is active.

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
<td>Decrease widths on pairs is active.</td>
</tr>
<tr>
<td><b>tomFalse</b></td>
<td>Decrease widths on pairs is not active.</td>
</tr>
<tr>
<td><b>tomUndefined</b></td>
<td>The ModWidthPairs property is undefined.</td>
</tr>
</table>

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextfont2">ITextFont2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextfont2-setmodwidthpairs">ITextFont2::SetModWidthPairs</a>