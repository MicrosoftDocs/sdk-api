---
UID: NF:ctfutb.ITfLangBarItemBitmapButton.OnClick
title: ITfLangBarItemBitmapButton::OnClick (ctfutb.h)
description: This method is not used if the button item does not have the TF_LBI_STYLE_BTN_BUTTON style. (ITfLangBarItemBitmapButton.OnClick)
helpviewer_keywords: ["ITfLangBarItemBitmapButton interface [Text Services Framework]","OnClick method","ITfLangBarItemBitmapButton.OnClick","ITfLangBarItemBitmapButton::OnClick","OnClick","OnClick method [Text Services Framework]","OnClick method [Text Services Framework]","ITfLangBarItemBitmapButton interface","_tsf_itflangbaritembitmapbutton_onclick_ref","ctfutb/ITfLangBarItemBitmapButton::OnClick","tsf.itflangbaritembitmapbutton_onclick"]
old-location: tsf\itflangbaritembitmapbutton_onclick.htm
tech.root: TSF
ms.assetid: 8d376d22-897d-4032-9c9e-7d0f93d73fac
ms.date: 12/05/2018
ms.keywords: ITfLangBarItemBitmapButton interface [Text Services Framework],OnClick method, ITfLangBarItemBitmapButton.OnClick, ITfLangBarItemBitmapButton::OnClick, OnClick, OnClick method [Text Services Framework], OnClick method [Text Services Framework],ITfLangBarItemBitmapButton interface, _tsf_itflangbaritembitmapbutton_onclick_ref, ctfutb/ITfLangBarItemBitmapButton::OnClick, tsf.itflangbaritembitmapbutton_onclick
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
 - ITfLangBarItemBitmapButton::OnClick
 - ctfutb/ITfLangBarItemBitmapButton::OnClick
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
 - ITfLangBarItemBitmapButton.OnClick
---

# ITfLangBarItemBitmapButton::OnClick


## -description

This method is not used if the button item does not have the TF_LBI_STYLE_BTN_BUTTON style.

## -parameters

### -param click [in]

Contains a <a href="/windows/win32/api/ctfutb/ne-ctfutb-tflbiclick">TfLBIClick</a> value that indicates which mouse button was used to click the button.

### -param pt [in]

Pointer to a <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure that contains the position, in screen coordinates, of the mouse cursor at the time of the click event.

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

<a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritembitmapbutton">ITfLangBarItemBitmapButton</a>



<a href="/windows/win32/api/windef/ns-windef-point">POINT</a>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>



<a href="/windows/win32/api/ctfutb/ne-ctfutb-tflbiclick">TfLBIClick
      </a>
