---
UID: NF:tom.ITextPara2.SetFontAlignment
title: ITextPara2::SetFontAlignment (tom.h)
description: Sets the paragraph font alignment for Chinese, Japanese, Korean text.
helpviewer_keywords: ["ITextPara2 interface [Windows Controls]","SetFontAlignment method","ITextPara2.SetFontAlignment","ITextPara2::SetFontAlignment","SetFontAlignment","SetFontAlignment method [Windows Controls]","SetFontAlignment method [Windows Controls]","ITextPara2 interface","controls.itextpara2_setfontalignment","tom/ITextPara2::SetFontAlignment"]
old-location: controls\itextpara2_setfontalignment.htm
tech.root: Controls
ms.assetid: 2ed1f7f2-9523-4dda-bac0-c1eb3d217102
ms.date: 12/05/2018
ms.keywords: ITextPara2 interface [Windows Controls],SetFontAlignment method, ITextPara2.SetFontAlignment, ITextPara2::SetFontAlignment, SetFontAlignment, SetFontAlignment method [Windows Controls], SetFontAlignment method [Windows Controls],ITextPara2 interface, controls.itextpara2_setfontalignment, tom/ITextPara2::SetFontAlignment
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
 - ITextPara2::SetFontAlignment
 - tom/ITextPara2::SetFontAlignment
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
 - ITextPara2.SetFontAlignment
---

# ITextPara2::SetFontAlignment


## -description

Sets the paragraph font alignment for Chinese, Japanese, Korean text.

## -parameters

### -param Value [in]

Type: <b>long</b>

The paragraph font alignment. It can be one of the following values.


<table>
<tr>
<th>Font Alignment States</th>
</tr>
<tr>
<td><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomFontAlignmentAuto</a> (default)</td>
</tr>
<tr>
<td><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomFontAlignmentTop</a></td>
</tr>
<tr>
<td><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomFontAlignmentBaseline</a></td>
</tr>
<tr>
<td><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomFontAlignmentBottom</a></td>
</tr>
<tr>
<td><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomFontAlignmentCenter</a></td>
</tr>
</table>

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextpara2">ITextPara2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextpara2-getfontalignment">ITextPara2::GetFontAlignment</a>