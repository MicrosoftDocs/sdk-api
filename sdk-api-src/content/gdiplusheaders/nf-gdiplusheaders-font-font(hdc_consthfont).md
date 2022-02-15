---
UID: NF:gdiplusheaders.Font.Font(HDC,constHFONT)
title: Font::Font(IN HDC,IN const HFONT) (gdiplusheaders.h)
description: Creates a Font::Font object indirectly from a Windows Graphics Device Interface (GDI) logical font by using a handle to a GDILOGFONT structure.
helpviewer_keywords: ["Font","Font class [GDI+]","Font constructor","Font constructor [GDI+]","Font constructor [GDI+]","Font class","Font.Font","Font.Font(HDC","const HFONT)","Font.Font(IN HDC","IN const HFONT)","Font::Font","Font::Font(IN HDC","IN const HFONT)","_gdiplus_CLASS_Font_Font_hdc_hfont_","gdiplus._gdiplus_CLASS_Font_Font_hdc_hfont_"]
old-location: gdiplus\_gdiplus_CLASS_Font_Font_hdc_hfont_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\fontclass\fontconstructors\font_2hdc_hfont.htm
ms.date: 12/05/2018
ms.keywords: Font, Font class [GDI+],Font constructor, Font constructor [GDI+], Font constructor [GDI+],Font class, Font.Font, Font.Font(HDC,const HFONT), Font.Font(IN HDC,IN const HFONT), Font::Font, Font::Font(IN HDC,IN const HFONT), _gdiplus_CLASS_Font_Font_hdc_hfont_, gdiplus._gdiplus_CLASS_Font_Font_hdc_hfont_
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

# Font::Font(IN HDC,IN const HFONT)


## -description

Creates a <b>Font::Font</b> object indirectly from a Windows Graphics Device Interface (GDI) logical font by using a handle to a GDI <b>LOGFONT</b> structure.

## -parameters

### -param hdc [in]

Type: <b>HDC</b>

Handle to a Windows device context. A handle is a number that Windows uses internally to reference an object.

### -param hfont [in]

Type: <b>const HFONT</b>

Handle to a logical font.

## -remarks

A device context is a structure that is maintained internally. It is associated with a particular device, such as a video monitor or a printer. There is usually one device context associated with each window displayed on a video monitor. A device context contains some graphics attributes used by GDI+.

