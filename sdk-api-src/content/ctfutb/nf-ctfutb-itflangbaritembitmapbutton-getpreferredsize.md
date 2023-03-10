---
UID: NF:ctfutb.ITfLangBarItemBitmapButton.GetPreferredSize
title: ITfLangBarItemBitmapButton::GetPreferredSize (ctfutb.h)
description: ITfLangBarItemBitmapButton::GetPreferredSize method
helpviewer_keywords: ["GetPreferredSize","GetPreferredSize method [Text Services Framework]","GetPreferredSize method [Text Services Framework]","ITfLangBarItemBitmapButton interface","ITfLangBarItemBitmapButton interface [Text Services Framework]","GetPreferredSize method","ITfLangBarItemBitmapButton.GetPreferredSize","ITfLangBarItemBitmapButton::GetPreferredSize","_tsf_itflangbaritembitmapbutton_getpreferredsize_ref","ctfutb/ITfLangBarItemBitmapButton::GetPreferredSize","tsf.itflangbaritembitmapbutton_getpreferredsize"]
old-location: tsf\itflangbaritembitmapbutton_getpreferredsize.htm
tech.root: TSF
ms.assetid: 271e4e24-c81e-484c-84bb-d7b67038a5c5
ms.date: 12/05/2018
ms.keywords: GetPreferredSize, GetPreferredSize method [Text Services Framework], GetPreferredSize method [Text Services Framework],ITfLangBarItemBitmapButton interface, ITfLangBarItemBitmapButton interface [Text Services Framework],GetPreferredSize method, ITfLangBarItemBitmapButton.GetPreferredSize, ITfLangBarItemBitmapButton::GetPreferredSize, _tsf_itflangbaritembitmapbutton_getpreferredsize_ref, ctfutb/ITfLangBarItemBitmapButton::GetPreferredSize, tsf.itflangbaritembitmapbutton_getpreferredsize
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
 - ITfLangBarItemBitmapButton::GetPreferredSize
 - ctfutb/ITfLangBarItemBitmapButton::GetPreferredSize
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
 - ITfLangBarItemBitmapButton.GetPreferredSize
---

# ITfLangBarItemBitmapButton::GetPreferredSize


## -description

Obtains the preferred size, in pixels, of the bitmap.

## -parameters

### -param pszDefault [in]

Pointer to a <a href="/windows/win32/api/windef/ns-windef-size">SIZE</a> structure that contains the default size, in pixels, of the bitmap.

### -param psz [out]

Pointer to a SIZE structure that receives the preferred size, in pixels, of the bitmap. The <b>cy</b> member of this structure is ignored.

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
</table>

## -remarks

The results of this method are not currently used. The bitmap for a bitmap button item should not be larger than the size of a small icon. Obtain these dimensions by calling <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics">GetSystemMetrics</a> with SM_CXSMICON for the width and SM_CYSMICON for the height.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics">GetSystemMetrics</a>



<a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritembitmapbutton">ITfLangBarItemBitmapButton</a>



<a href="/windows/win32/api/windef/ns-windef-size">SIZE</a>