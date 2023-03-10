---
UID: NF:ctfutb.ITfLangBarItemButton.OnClick
title: ITfLangBarItemButton::OnClick (ctfutb.h)
description: This method is not used if the button item does not have the TF_LBI_STYLE_BTN_BUTTON style. (ITfLangBarItemButton.OnClick)
helpviewer_keywords: ["ITfLangBarItemButton interface [Text Services Framework]","OnClick method","ITfLangBarItemButton.OnClick","ITfLangBarItemButton::OnClick","OnClick","OnClick method [Text Services Framework]","OnClick method [Text Services Framework]","ITfLangBarItemButton interface","_tsf_itflangbaritembutton_onclick_ref","ctfutb/ITfLangBarItemButton::OnClick","tsf.itflangbaritembutton_onclick"]
old-location: tsf\itflangbaritembutton_onclick.htm
tech.root: TSF
ms.assetid: c725ee0b-57fe-4860-aa49-af61f2c7fa32
ms.date: 12/05/2018
ms.keywords: ITfLangBarItemButton interface [Text Services Framework],OnClick method, ITfLangBarItemButton.OnClick, ITfLangBarItemButton::OnClick, OnClick, OnClick method [Text Services Framework], OnClick method [Text Services Framework],ITfLangBarItemButton interface, _tsf_itflangbaritembutton_onclick_ref, ctfutb/ITfLangBarItemButton::OnClick, tsf.itflangbaritembutton_onclick
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
 - ITfLangBarItemButton::OnClick
 - ctfutb/ITfLangBarItemButton::OnClick
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
 - ITfLangBarItemButton.OnClick
---

# ITfLangBarItemButton::OnClick


## -description

This method is not used if the button item does not have the TF_LBI_STYLE_BTN_BUTTON style.

## -parameters

### -param click [in]

Contains one of the <a href="/windows/win32/api/ctfutb/ne-ctfutb-tflbiclick">TfLBIClick</a> values that indicate which mouse button was used to click the button.

### -param pt [in]

Pointer to a <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure that contains the position of the mouse cursor, in screen coordinates, at the time of the click event.

### -param prcArea [in]

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that contains the bounding rectangle, in screen coordinates, of the button.

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

<a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritembutton">ITfLangBarItemButton</a>



<a href="/windows/win32/api/windef/ns-windef-point">POINT</a>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>



<a href="/windows/win32/api/ctfutb/ne-ctfutb-tflbiclick">TfLBIClick
      </a>
