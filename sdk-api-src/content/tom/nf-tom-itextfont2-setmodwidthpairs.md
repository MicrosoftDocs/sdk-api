---
UID: NF:tom.ITextFont2.SetModWidthPairs
title: ITextFont2::SetModWidthPairs (tom.h)
description: Sets whether &quot;decrease widths on pairs&quot; is active.
helpviewer_keywords: ["ITextFont2 interface [Windows Controls]","SetModWidthPairs method","ITextFont2.SetModWidthPairs","ITextFont2::SetModWidthPairs","SetModWidthPairs","SetModWidthPairs method [Windows Controls]","SetModWidthPairs method [Windows Controls]","ITextFont2 interface","controls.itextfont2_setmodwidthpairs","tom/ITextFont2::SetModWidthPairs"]
old-location: controls\itextfont2_setmodwidthpairs.htm
tech.root: Controls
ms.assetid: 60117c84-18f9-49db-8d13-b55576874d2b
ms.date: 12/05/2018
ms.keywords: ITextFont2 interface [Windows Controls],SetModWidthPairs method, ITextFont2.SetModWidthPairs, ITextFont2::SetModWidthPairs, SetModWidthPairs, SetModWidthPairs method [Windows Controls], SetModWidthPairs method [Windows Controls],ITextFont2 interface, controls.itextfont2_setmodwidthpairs, tom/ITextFont2::SetModWidthPairs
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
 - ITextFont2::SetModWidthPairs
 - tom/ITextFont2::SetModWidthPairs
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
 - ITextFont2.SetModWidthPairs
---

# ITextFont2::SetModWidthPairs


## -description

Sets whether "decrease widths on pairs" is active.

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
<td>Decrease widths on pairs is active.</td>
</tr>
<tr>
<td><b>tomFalse</b></td>
<td>Decrease widths on pairs is not active.</td>
</tr>
<tr>
<td><b>tomToggle</b></td>
<td>Toggle the ModWidthPairs property.</td>
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



<a href="/windows/desktop/api/tom/nf-tom-itextfont2-getmodwidthpairs">ITextFont2::GetModWidthPairs</a>