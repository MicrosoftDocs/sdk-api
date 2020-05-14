---
UID: NS:wingdi.tagPOLYTEXTW
title: POLYTEXTW (wingdi.h)
description: The POLYTEXT structure describes how the PolyTextOut function should draw a string of text.helpviewer_keywords: ["*LPPOLYTEXTW","*NPPOLYTEXTW","*PPOLYTEXTW","POLYTEXT","POLYTEXT structure [Windows GDI]","POLYTEXTA","POLYTEXTW","PPOLYTEXT","PPOLYTEXT structure pointer [Windows GDI]","_win32_POLYTEXT_str","gdi.polytext","wingdi/POLYTEXT","wingdi/POLYTEXTA","wingdi/POLYTEXTW","wingdi/PPOLYTEXT"]
old-location: gdi\polytext.htm
tech.root: gdi
ms.assetid: 6f03e2ff-c15f-498c-8c3d-33106222279e
ms.date: 12/05/2018
ms.keywords: '*LPPOLYTEXTW, *NPPOLYTEXTW, *PPOLYTEXTW, POLYTEXT, POLYTEXT structure [Windows GDI], POLYTEXTA, POLYTEXTW, PPOLYTEXT, PPOLYTEXT structure pointer [Windows GDI], _win32_POLYTEXT_str, gdi.polytext, wingdi/POLYTEXT, wingdi/POLYTEXTA, wingdi/POLYTEXTW, wingdi/PPOLYTEXT'
f1_keywords:
- wingdi/POLYTEXT
dev_langs:
- c++
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: POLYTEXTW (Unicode) and POLYTEXTA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Wingdi.h
api_name:
- POLYTEXT
- POLYTEXTA
- POLYTEXTW
targetos: Windows
req.typenames: POLYTEXTW, *PPOLYTEXTW, *NPPOLYTEXTW, *LPPOLYTEXTW
req.redist: 
ms.custom: 19H1
---

# POLYTEXTW structure


## -description



The <b>POLYTEXT</b> structure describes how the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-polytextouta">PolyTextOut</a> function should draw a string of text.




## -struct-fields




### -field x

The horizontal reference point for the string. The string is aligned to this point using the current text-alignment mode.


### -field y

The vertical reference point for the string. The string is aligned to this point using the current text-alignment mode.


### -field n

The <a href="https://docs.microsoft.com/windows/desktop/gdi/specifying-length-of-text-output-string">length of the string</a> pointed to by <b>lpstr</b>.


### -field lpstr

Pointer to a string of text to be drawn by the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-polytextouta">PolyTextOut</a> function. This string need not be null-terminated, since <b>n</b> specifies the length of the string.


### -field uiFlags

Specifies whether the string is to be opaque or clipped and whether the string is accompanied by an array of character-width values. This member can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>ETO_OPAQUE</td>
<td>The rectangle for each string is to be opaqued with the current background color.</td>
</tr>
<tr>
<td>ETO_CLIPPED</td>
<td>Each string is to be clipped to its specified rectangle.</td>
</tr>
</table>
 


### -field rcl

A rectangle structure that contains the dimensions of the opaquing or clipping rectangle. This member is ignored if neither of the ETO_OPAQUE nor the ETO_CLIPPED value is specified for the <b>uiFlags</b> member.


### -field pdx

Pointer to an array containing the width value for each character in the string.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/gdi/font-and-text-structures">Font and Text Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-polytextouta">PolyTextOut</a>
 

 

