---
UID: NF:tom.ITextFont2.GetOldNumbers
title: ITextFont2::GetOldNumbers (tom.h)
description: Gets whether old-style numbers are active.
helpviewer_keywords: ["GetOldNumbers","GetOldNumbers method [Windows Controls]","GetOldNumbers method [Windows Controls]","ITextFont2 interface","ITextFont2 interface [Windows Controls]","GetOldNumbers method","ITextFont2.GetOldNumbers","ITextFont2::GetOldNumbers","controls.itextfont2_getoldnumbers","tom/ITextFont2::GetOldNumbers"]
old-location: controls\itextfont2_getoldnumbers.htm
tech.root: Controls
ms.assetid: 8e800840-5ca2-4fbf-94c2-d51aa73bf188
ms.date: 12/05/2018
ms.keywords: GetOldNumbers, GetOldNumbers method [Windows Controls], GetOldNumbers method [Windows Controls],ITextFont2 interface, ITextFont2 interface [Windows Controls],GetOldNumbers method, ITextFont2.GetOldNumbers, ITextFont2::GetOldNumbers, controls.itextfont2_getoldnumbers, tom/ITextFont2::GetOldNumbers
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
 - ITextFont2::GetOldNumbers
 - tom/ITextFont2::GetOldNumbers
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
 - ITextFont2.GetOldNumbers
---

# ITextFont2::GetOldNumbers


## -description

Gets whether old-style numbers are active.

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
<td>Old-style numbers are active.</td>
</tr>
<tr>
<td><b>tomFalse</b></td>
<td>Old-style numbers are not active.</td>
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



<a href="/windows/desktop/api/tom/nf-tom-itextfont2-setoldnumbers">ITextFont2::SetOldNumbers</a>