---
UID: NF:gdiplusheaders.Font.GetLogFontA
title: Font::GetLogFontA (gdiplusheaders.h)
description: The Font::GetLogFontA method uses a LOGFONTA structure to get the attributes of this Font object.
helpviewer_keywords: ["Font class [GDI+]", "GetLogFontA method", "Font.GetLogFontA", "Font::GetLogFontA", "GetLogFontA", "GetLogFontA method [GDI+]", "GetLogFontA method [GDI+]", "Font class", "_gdiplus_CLASS_Font_GetLogFontA_g_logfontA_", "gdiplus._gdiplus_CLASS_Font_GetLogFontA_g_logfontA_"]
old-location: gdiplus\_gdiplus_CLASS_Font_GetLogFontA_g_logfontA_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\fontclass\fontmethods\getlogfonta.htm
ms.date: 12/05/2018
ms.keywords: Font class [GDI+],GetLogFontA method, Font.GetLogFontA, Font::GetLogFontA, GetLogFontA, GetLogFontA method [GDI+], GetLogFontA method [GDI+],Font class, _gdiplus_CLASS_Font_GetLogFontA_g_logfontA_, gdiplus._gdiplus_CLASS_Font_GetLogFontA_g_logfontA_
req.header: gdiplusheaders.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
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
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - Font::GetLogFontA
 - gdiplusheaders/Font::GetLogFontA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Font.GetLogFontA
 - getlogfonta
---

# Font::GetLogFontA


## -description

The <b>Font::GetLogFontA</b> method uses a 
			<b>LOGFONTA</b> structure to get the attributes of this 
			<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font">Font</a> object.

## -parameters

### -param g [in]

Type: <b>const <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object that contains attributes of the display device.

### -param logfontA [out]

Type: <b>LOGFONTA*</b>

Pointer to a 
					<b>LOGFONTA</b> structure variable that receives the font attributes.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font">Font</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-text-and-fonts-use">Using Text and Fonts</a>
