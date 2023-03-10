---
UID: NF:gdiplusheaders.Font.Font(HDC)
title: Font::Font(IN HDC) (gdiplusheaders.h)
description: Creates a Font::Font object based on the Windows Graphics Device Interface (GDI) font object that is currently selected into a specified device context. This constructor is provided for compatibility with GDI.
helpviewer_keywords: ["Font","Font class [GDI+]","Font constructor","Font constructor [GDI+]","Font constructor [GDI+]","Font class","Font.Font","Font.Font(HDC)","Font.Font(IN HDC)","Font::Font","Font::Font(IN HDC)","_gdiplus_CLASS_Font_Font_hdc_","gdiplus._gdiplus_CLASS_Font_Font_hdc_"]
old-location: gdiplus\_gdiplus_CLASS_Font_Font_hdc_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\fontclass\fontconstructors\font_8hdc.htm
ms.date: 12/05/2018
ms.keywords: Font, Font class [GDI+],Font constructor, Font constructor [GDI+], Font constructor [GDI+],Font class, Font.Font, Font.Font(HDC), Font.Font(IN HDC), Font::Font, Font::Font(IN HDC), _gdiplus_CLASS_Font_Font_hdc_, gdiplus._gdiplus_CLASS_Font_Font_hdc_
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
 - Font::Font
 - gdiplusheaders/Font::Font
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
 - Font.Font
---

# Font::Font(IN HDC)


## -description

Creates a <b>Font::Font</b> object based on the Windows Graphics Device Interface (GDI) font object that is currently selected into a specified device context. This constructor is provided for compatibility with GDI.

## -parameters

### -param hdc [in]

Type: <b>HDC</b>

Handle to a Windows device context that has a font selected. A handle is a number that Windows uses internally to reference an object.

## -remarks

In most cases when you obtain a device context handle by calling the 
				<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-gethdc">GetHDC</a> method of a 
				<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object, the device context will not have a font selected. If you pass such a handle to this constructor, the constructor will fail.

A device context is a structure that is maintained internally. It is associated with a particular device, such as a video monitor or a printer. There is usually one device context associated with each window displayed on a video monitor. A device context contains some graphics attributes used by GDI+.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-changes-in-the-programming-model-about">Changes in the Programming Model</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font">Font</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-text-and-fonts-use">Using Text and Fonts</a>