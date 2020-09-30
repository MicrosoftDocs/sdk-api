---
UID: NF:vfw.DrawDibProfileDisplay
title: DrawDibProfileDisplay function (vfw.h)
description: The DrawDibProfileDisplay function determines settings for the display system when using DrawDib functions.
helpviewer_keywords: ["DrawDibProfileDisplay","DrawDibProfileDisplay function [Windows Multimedia]","_win32_DrawDibProfileDisplay","multimedia.drawdibprofiledisplay","vfw/DrawDibProfileDisplay"]
old-location: multimedia\drawdibprofiledisplay.htm
tech.root: Multimedia
ms.assetid: 51f8b1a2-26e2-40d3-bbc0-5c6c1b482014
ms.date: 12/05/2018
ms.keywords: DrawDibProfileDisplay, DrawDibProfileDisplay function [Windows Multimedia], _win32_DrawDibProfileDisplay, multimedia.drawdibprofiledisplay, vfw/DrawDibProfileDisplay
req.header: vfw.h
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
req.lib: Vfw32.lib
req.dll: Msvfw32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DrawDibProfileDisplay
 - vfw/DrawDibProfileDisplay
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msvfw32.dll
api_name:
 - DrawDibProfileDisplay
---

# DrawDibProfileDisplay function


## -description

The <b>DrawDibProfileDisplay</b> function determines settings for the display system when using DrawDib functions.

## -parameters

### -param lpbi

Pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure that contains bitmap information. You can also specify <b>NULL</b> to verify that the profile information is current. If the profile information is not current, DrawDib will rerun the profile tests to obtain a current set of information. When you call <b>DrawDibProfileDisplay</b> with this parameter set to <b>NULL</b>, the return value is meaningless.

## -returns

Returns a value that indicates the fastest drawing and stretching capabilities of the display system. This value can be zero if the bitmap format is not supported or one or more of the following values.
          

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PD_CAN_DRAW_DIB</b></dt>
</dl>
</td>
<td width="60%">
DrawDib can draw images using this format. Stretching might or might not also be supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PD_CAN_STRETCHDIB</b></dt>
</dl>
</td>
<td width="60%">
DrawDib can stretch and draw images using this format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PD_STRETCHDIB_1_1_OK</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/wingdi/nf-wingdi-stretchdibits">StretchDIBits</a> draws unstretched images using this format faster than an alternative method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PD_STRETCHDIB_1_2_OK</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/wingdi/nf-wingdi-stretchdibits">StretchDIBits</a> draws stretched images (in a 1:2 ratio) using this format faster than an alternative method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PD_STRETCHDIB_1_N_OK</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/wingdi/nf-wingdi-stretchdibits">StretchDIBits</a> draws stretched images (in a 1:N ratio) using this format faster than an alternative method.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/Multimedia/drawdib-functions">DrawDib Functions</a>