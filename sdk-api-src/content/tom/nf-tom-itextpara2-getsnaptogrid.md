---
UID: NF:tom.ITextPara2.GetSnapToGrid
title: ITextPara2::GetSnapToGrid (tom.h)
description: Gets whether paragraph lines snap to a vertical grid that could be defined for the whole document.
helpviewer_keywords: ["GetSnapToGrid","GetSnapToGrid method [Windows Controls]","GetSnapToGrid method [Windows Controls]","ITextPara2 interface","ITextPara2 interface [Windows Controls]","GetSnapToGrid method","ITextPara2.GetSnapToGrid","ITextPara2::GetSnapToGrid","controls.itextpara2_getsnaptogrid","tom/ITextPara2::GetSnapToGrid"]
old-location: controls\itextpara2_getsnaptogrid.htm
tech.root: Controls
ms.assetid: ee5fd1d8-cd2d-4674-bb0f-6021a3115aac
ms.date: 12/05/2018
ms.keywords: GetSnapToGrid, GetSnapToGrid method [Windows Controls], GetSnapToGrid method [Windows Controls],ITextPara2 interface, ITextPara2 interface [Windows Controls],GetSnapToGrid method, ITextPara2.GetSnapToGrid, ITextPara2::GetSnapToGrid, controls.itextpara2_getsnaptogrid, tom/ITextPara2::GetSnapToGrid
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
 - ITextPara2::GetSnapToGrid
 - tom/ITextPara2::GetSnapToGrid
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
 - ITextPara2.GetSnapToGrid
---

# ITextPara2::GetSnapToGrid


## -description

Gets whether paragraph lines snap to a vertical grid that could be defined for the whole document.

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
<td>Paragraph lines snap to a vertical grid.</td>
</tr>
<tr>
<td><b>tomFalse</b></td>
<td>Paragraph lines do not snap to a grid.</td>
</tr>
<tr>
<td><b>tomUndefined</b></td>
<td>The SnapToGrid property is undefined.</td>
</tr>
</table>

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextpara2">ITextPara2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextpara2-setsnaptogrid">ITextPara2::SetSnapToGrid</a>