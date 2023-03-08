---
UID: NF:ctfutb.ITfLangBarItemBalloon.GetPreferredSize
title: ITfLangBarItemBalloon::GetPreferredSize (ctfutb.h)
description: ITfLangBarItemBalloon::GetPreferredSize method
helpviewer_keywords: ["GetPreferredSize","GetPreferredSize method [Text Services Framework]","GetPreferredSize method [Text Services Framework]","ITfLangBarItemBalloon interface","ITfLangBarItemBalloon interface [Text Services Framework]","GetPreferredSize method","ITfLangBarItemBalloon.GetPreferredSize","ITfLangBarItemBalloon::GetPreferredSize","_tsf_itflangbaritemballoon_getpreferredsize_ref","ctfutb/ITfLangBarItemBalloon::GetPreferredSize","tsf.itflangbaritemballoon_getpreferredsize"]
old-location: tsf\itflangbaritemballoon_getpreferredsize.htm
tech.root: TSF
ms.assetid: 73f3a12e-b787-424e-9998-276baee63264
ms.date: 12/05/2018
ms.keywords: GetPreferredSize, GetPreferredSize method [Text Services Framework], GetPreferredSize method [Text Services Framework],ITfLangBarItemBalloon interface, ITfLangBarItemBalloon interface [Text Services Framework],GetPreferredSize method, ITfLangBarItemBalloon.GetPreferredSize, ITfLangBarItemBalloon::GetPreferredSize, _tsf_itflangbaritemballoon_getpreferredsize_ref, ctfutb/ITfLangBarItemBalloon::GetPreferredSize, tsf.itflangbaritemballoon_getpreferredsize
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
 - ITfLangBarItemBalloon::GetPreferredSize
 - ctfutb/ITfLangBarItemBalloon::GetPreferredSize
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
 - ITfLangBarItemBalloon.GetPreferredSize
---

# ITfLangBarItemBalloon::GetPreferredSize


## -description

Obtains the preferred size,in pixels, of the balloon.

## -parameters

### -param pszDefault [in]

Pointer to a <a href="/windows/win32/api/windef/ns-windef-size">SIZE</a> structure that contains the default size, in pixels, of the balloon.

### -param psz [out]

Pointer to a <b>SIZE</b> structure that receives the preferred balloon size, in pixels. The <b>cy</b> member of this structure is ignored.

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

This method is required. The balloon must supply the preferred size in response to this method.

To obtain the font used to draw the balloon, call <a href="/windows/desktop/api/wingdi/nf-wingdi-getstockobject">GetStockObject</a> with DEFAULT_GUI_FONT. This font can be used to calculate the preferred balloon size at runtime.

If the balloon text will not fit into the preferred size obtained from this method, the language bar truncates the text and adds an ellipses to the text.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-getstockobject">GetStockObject</a>



<a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritemballoon">ITfLangBarItemBalloon</a>



<a href="/windows/win32/api/windef/ns-windef-size">SIZE</a>