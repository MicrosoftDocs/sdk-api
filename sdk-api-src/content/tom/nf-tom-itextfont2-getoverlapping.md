---
UID: NF:tom.ITextFont2.GetOverlapping
title: ITextFont2::GetOverlapping (tom.h)
description: Gets whether overlapping text is active.
helpviewer_keywords: ["GetOverlapping","GetOverlapping method [Windows Controls]","GetOverlapping method [Windows Controls]","ITextFont2 interface","ITextFont2 interface [Windows Controls]","GetOverlapping method","ITextFont2.GetOverlapping","ITextFont2::GetOverlapping","controls.itextfont2_getoverlapping","tom/ITextFont2::GetOverlapping"]
old-location: controls\itextfont2_getoverlapping.htm
tech.root: Controls
ms.assetid: 26937777-a44b-4196-aa6b-f35787f934a9
ms.date: 12/05/2018
ms.keywords: GetOverlapping, GetOverlapping method [Windows Controls], GetOverlapping method [Windows Controls],ITextFont2 interface, ITextFont2 interface [Windows Controls],GetOverlapping method, ITextFont2.GetOverlapping, ITextFont2::GetOverlapping, controls.itextfont2_getoverlapping, tom/ITextFont2::GetOverlapping
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
 - ITextFont2::GetOverlapping
 - tom/ITextFont2::GetOverlapping
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
 - ITextFont2.GetOverlapping
---

# ITextFont2::GetOverlapping


## -description

Gets whether overlapping text is active.

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
<td>Overlapping text is active.</td>
</tr>
<tr>
<td><b>tomFalse</b></td>
<td>Overlapping text is not active.</td>
</tr>
<tr>
<td><b>tomUndefined</b></td>
<td>The Overlapping property is undefined.</td>
</tr>
</table>

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextfont2">ITextFont2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextfont2-setoverlapping">ITextFont2::SetOverlapping</a>