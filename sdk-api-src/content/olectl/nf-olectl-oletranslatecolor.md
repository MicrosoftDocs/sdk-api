---
UID: NF:olectl.OleTranslateColor
title: OleTranslateColor function (olectl.h)
description: Converts an OLE_COLOR type to a COLORREF.
helpviewer_keywords: ["OleTranslateColor","OleTranslateColor function [COM]","_ctrl_OleTranslateColor","com.oletranslatecolor","olectl/OleTranslateColor"]
old-location: com\oletranslatecolor.htm
tech.root: com
ms.assetid: f4b407c3-e88a-47b4-bb43-8f691629d2f3
ms.date: 12/05/2018
ms.keywords: OleTranslateColor, OleTranslateColor function [COM], _ctrl_OleTranslateColor, com.oletranslatecolor, olectl/OleTranslateColor
req.header: olectl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - OleTranslateColor
 - olectl/OleTranslateColor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - OleTranslateColor
---

# OleTranslateColor function


## -description

Converts an <b>OLE_COLOR</b> type to a <b>COLORREF</b>.

## -parameters

### -param clr [in]

The OLE color to be converted into a <b>COLORREF</b>.

### -param hpal [in]

Palette used as a basis for the conversion.

### -param lpcolorref [out]

Pointer to the caller's variable that receives the converted <b>COLORREF</b> result. This parameter can be <b>NULL</b>, indicating that the caller wants only to verify that a converted color exists.

## -returns

This function supports the standard return values E_INVALIDARG and E_UNEXPECTED, as well as the following value.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The color was translated successfully.

</td>
</tr>
</table>

## -remarks

The following table describes the color conversion.

<table>
<tr>
<th>OLE_COLOR</th>
<th>hPal</th>
<th>COLORREF</th>
</tr>
<tr>
<td>invalid
</td>
<td></td>
<td>Undefined (E_INVALIDARG)
</td>
</tr>
<tr>
<td>0x800000xx, xx is not a valid <a href="/windows/desktop/api/winuser/nf-winuser-getsyscolor">GetSysColor</a> index
</td>
<td></td>
<td>Undefined (E_INVALIDARG)
</td>
</tr>
<tr>
<td></td>
<td>invalid
</td>
<td>Undefined (E_INVALIDARG)
</td>
</tr>
<tr>
<td>  0x0100iiii, iiii is not a valid palette index
 
</td>
<td>valid palette
</td>
<td>Undefined (E_INVALIDARG)
</td>
</tr>
<tr>
<td>0x800000xx, xx is a valid <a href="/windows/desktop/api/winuser/nf-winuser-getsyscolor">GetSysColor</a> index
</td>
<td><b>NULL</b></td>
<td>0x00bbggrr
</td>
</tr>
<tr>
<td>0x0100iiii, iiii is a valid palette index
</td>
<td><b>NULL</b></td>
<td>0x0100iiii
</td>
</tr>
<tr>
<td>0x02bbggrr (palette relative)
</td>
<td><b>NULL</b></td>
<td>0x02bbggrr
</td>
</tr>
<tr>
<td>0x00bbggrr
</td>
<td><b>NULL</b></td>
<td>0x00bbggrr
</td>
</tr>
<tr>
<td>0x800000xx, xx is a valid <a href="/windows/desktop/api/winuser/nf-winuser-getsyscolor">GetSysColor</a> index
</td>
<td>valid palette
</td>
<td>0x00bbggrr
</td>
</tr>
<tr>
<td>0x0100iiii, iiii is a valid palette index in hPal
</td>
<td>valid palette
</td>
<td>0x0100iiii
</td>
</tr>
<tr>
<td>0x02bbggrr (palette relative)
</td>
<td>valid palette
</td>
<td>0x02bbggrr
</td>
</tr>
<tr>
<td>0x00bbggrr
</td>
<td>valid palette
</td>
<td>0x02bbggrr
</td>
</tr>
</table>