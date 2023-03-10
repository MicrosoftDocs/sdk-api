---
UID: NF:ctfutb.ITfLangBarItemBitmap.OnClick
title: ITfLangBarItemBitmap::OnClick (ctfutb.h)
description: ITfLangBarItemBitmap::OnClick method
helpviewer_keywords: ["ITfLangBarItemBitmap interface [Text Services Framework]","OnClick method","ITfLangBarItemBitmap.OnClick","ITfLangBarItemBitmap::OnClick","OnClick","OnClick method [Text Services Framework]","OnClick method [Text Services Framework]","ITfLangBarItemBitmap interface","_tsf_itflangbaritembitmap_onclick_ref","ctfutb/ITfLangBarItemBitmap::OnClick","tsf.itflangbaritembitmap_onclick"]
old-location: tsf\itflangbaritembitmap_onclick.htm
tech.root: TSF
ms.assetid: b4e5857e-7e0b-462d-90cd-cb0e7b1143d5
ms.date: 12/05/2018
ms.keywords: ITfLangBarItemBitmap interface [Text Services Framework],OnClick method, ITfLangBarItemBitmap.OnClick, ITfLangBarItemBitmap::OnClick, OnClick, OnClick method [Text Services Framework], OnClick method [Text Services Framework],ITfLangBarItemBitmap interface, _tsf_itflangbaritembitmap_onclick_ref, ctfutb/ITfLangBarItemBitmap::OnClick, tsf.itflangbaritembitmap_onclick
req.header: ctfutb.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctfutb.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfLangBarItemBitmap::OnClick
 - ctfutb/ITfLangBarItemBitmap::OnClick
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfLangBarItemBitmap.OnClick
---

# ITfLangBarItemBitmap::OnClick


## -description

Not currently used.

## -parameters

### -param click [in]

Contains one of the <a href="/windows/win32/api/ctfutb/ne-ctfutb-tflbiclick">TfLBIClick</a> values that indicate which mouse button was used to click the bitmap.

### -param pt [in]

Pointer to a <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure that contains the position of the mouse cursor, in screen coordinates, at the time of the click event.

### -param prcArea [in]

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that contains the bounding rectangle, in screen coordinates, of the bitmap.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritembitmap">ITfLangBarItemBitmap</a>



<a href="/windows/win32/api/windef/ns-windef-point">POINT</a>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>



<a href="/windows/win32/api/ctfutb/ne-ctfutb-tflbiclick">TfLBIClick
      </a>