---
UID: NF:tom.ITextPara2.GetFontAlignment
title: ITextPara2::GetFontAlignment (tom.h)
description: Gets the paragraph font alignment state.
helpviewer_keywords: ["GetFontAlignment","GetFontAlignment method [Windows Controls]","GetFontAlignment method [Windows Controls]","ITextPara2 interface","ITextPara2 interface [Windows Controls]","GetFontAlignment method","ITextPara2.GetFontAlignment","ITextPara2::GetFontAlignment","controls.itextpara2_getfontalignment","tom/ITextPara2::GetFontAlignment"]
old-location: controls\itextpara2_getfontalignment.htm
tech.root: Controls
ms.assetid: 1064c033-2ae0-46ec-a670-603edd673e87
ms.date: 12/05/2018
ms.keywords: GetFontAlignment, GetFontAlignment method [Windows Controls], GetFontAlignment method [Windows Controls],ITextPara2 interface, ITextPara2 interface [Windows Controls],GetFontAlignment method, ITextPara2.GetFontAlignment, ITextPara2::GetFontAlignment, controls.itextpara2_getfontalignment, tom/ITextPara2::GetFontAlignment
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
 - ITextPara2::GetFontAlignment
 - tom/ITextPara2::GetFontAlignment
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
 - ITextPara2.GetFontAlignment
---

# ITextPara2::GetFontAlignment


## -description

Gets the paragraph font alignment state.

## -parameters

### -param pValue [out, retval]

Type: <b>long*</b>

The paragraph font alignment state. It can be one of the following values.

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



<a href="/windows/desktop/api/tom/nf-tom-itextpara2-setfontalignment">ITextPara2::SetFontAlignment</a>