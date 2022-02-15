---
UID: NF:ctfutb.ITfLangBarItemBitmapButton.DrawBitmap
title: ITfLangBarItemBitmapButton::DrawBitmap (ctfutb.h)
description: ITfLangBarItemBitmapButton::DrawBitmap method
helpviewer_keywords: ["DrawBitmap","DrawBitmap method [Text Services Framework]","DrawBitmap method [Text Services Framework]","ITfLangBarItemBitmapButton interface","ITfLangBarItemBitmapButton interface [Text Services Framework]","DrawBitmap method","ITfLangBarItemBitmapButton.DrawBitmap","ITfLangBarItemBitmapButton::DrawBitmap","_tsf_itflangbaritembitmapbutton_drawbitmap_ref","ctfutb/ITfLangBarItemBitmapButton::DrawBitmap","tsf.itflangbaritembitmapbutton_drawbitmap"]
old-location: tsf\itflangbaritembitmapbutton_drawbitmap.htm
tech.root: TSF
ms.assetid: 412b2e74-0569-4f72-bc8e-23edec72ea35
ms.date: 12/05/2018
ms.keywords: DrawBitmap, DrawBitmap method [Text Services Framework], DrawBitmap method [Text Services Framework],ITfLangBarItemBitmapButton interface, ITfLangBarItemBitmapButton interface [Text Services Framework],DrawBitmap method, ITfLangBarItemBitmapButton.DrawBitmap, ITfLangBarItemBitmapButton::DrawBitmap, _tsf_itflangbaritembitmapbutton_drawbitmap_ref, ctfutb/ITfLangBarItemBitmapButton::DrawBitmap, tsf.itflangbaritembitmapbutton_drawbitmap
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
 - ITfLangBarItemBitmapButton::DrawBitmap
 - ctfutb/ITfLangBarItemBitmapButton::DrawBitmap
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
 - ITfLangBarItemBitmapButton.DrawBitmap
---

# ITfLangBarItemBitmapButton::DrawBitmap


## -description

Obtains the bitmap and mask for the bitmap button item.

## -parameters

### -param bmWidth [in]

Contains the width, in pixels, of the bitmap button item.

### -param bmHeight [in]

Contains the height, in pixels, of the bitmap button item.

### -param dwFlags [in]

Not currently used.

### -param phbmp [out]

Pointer to an <b>HBITMAP</b> value that receives the handle of the bitmap drawn for the bitmap item.

### -param phbmpMask [out]

Pointer to an <b>HBITMAP</b> value that receives the handle of the mask bitmap. This is a monochrome bitmap that functions as a mask for <i>phbmp</i>. Each black pixel in this bitmap will cause the corresponding pixel in <i>phbmp</i> to be displayed in its normal color. Each white pixel in this bitmap will cause the cooresponding pixel in <i>phbmp</i> to be displayed in the inverse of its normal color.

To display the bitmap without color conversion, create a monochrome bitmap the same size as <i>phbmp</i> and set each pixel to black (RGB(0, 0, 0)).

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
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
</table>

