---
UID: NF:gdiplusheaders.Font.GetLogFontW
title: Font::GetLogFontW (gdiplusheaders.h)
description: The Font::GetLogFontW method uses a LOGFONTW structure to get the attributes of this Font object.
helpviewer_keywords: ["Font class [GDI+]", "GetLogFontW method", "Font.GetLogFontW", "Font::GetLogFontW", "GetLogFontW", "GetLogFontW method [GDI+]", "GetLogFontW method [GDI+]", "Font class", "_gdiplus_CLASS_Font_GetLogFontW_g_logfontW_", "gdiplus._gdiplus_CLASS_Font_GetLogFontW_g_logfontW_"]
old-location: gdiplus\_gdiplus_CLASS_Font_GetLogFontW_g_logfontW_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\fontclass\fontmethods\getlogfontw.htm
ms.date: 12/05/2018
ms.keywords: Font class [GDI+],GetLogFontW method, Font.GetLogFontW, Font::GetLogFontW, GetLogFontW, GetLogFontW method [GDI+], GetLogFontW method [GDI+],Font class, _gdiplus_CLASS_Font_GetLogFontW_g_logfontW_, gdiplus._gdiplus_CLASS_Font_GetLogFontW_g_logfontW_
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
 - Font::GetLogFontW
 - gdiplusheaders/Font::GetLogFontW
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
 - Font.GetLogFontW
 - getlogfontw
---

# Font::GetLogFontW


## -description

The <b>Font::GetLogFontW</b> method uses a 
			<b>LOGFONTW</b> structure to get the attributes of this 
			<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font">Font</a> object.

## -parameters

### -param g [in]

Type: <b>const <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object that contains attributes of the video display.

### -param logfontW [out]

Type: <b>LOGFONTW*</b>

Pointer to a 
					<b>LOGFONTW</b> structure variable that receives the font attributes.

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
