---
UID: NF:gdiplusheaders.Font.Font(INHDC,INconstLOGFONTA)
title: Font::Font(IN HDC,IN const LOGFONTA) (gdiplusheaders.h)
description: Creates a Font::Font object directly from a Windows Graphics Device Interface (GDI) logical font.
helpviewer_keywords: ["Font","Font class [GDI+]","Font constructor","Font constructor [GDI+]","Font constructor [GDI+]","Font class","Font.Font","Font.Font(HDC","const LOGFONTA*)","Font.Font(IN HDC","IN const LOGFONTA)","Font::Font","Font::Font(IN HDC","IN const LOGFONTA)","_gdiplus_CLASS_Font_Font_HDC_hdc_LOGFONTA_logfont_","gdiplus._gdiplus_CLASS_Font_Font_HDC_hdc_LOGFONTA_logfont_"]
old-location: gdiplus\_gdiplus_CLASS_Font_Font_HDC_hdc_LOGFONTA_logfont_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\fontclass\fontconstructors\font_53hdchdc_logfontalogfont.htm
ms.date: 12/05/2018
ms.keywords: Font, Font class [GDI+],Font constructor, Font constructor [GDI+], Font constructor [GDI+],Font class, Font.Font, Font.Font(HDC,const LOGFONTA*), Font.Font(IN HDC,IN const LOGFONTA), Font::Font, Font::Font(IN HDC,IN const LOGFONTA), _gdiplus_CLASS_Font_Font_HDC_hdc_LOGFONTA_logfont_, gdiplus._gdiplus_CLASS_Font_Font_HDC_hdc_LOGFONTA_logfont_
f1_keywords:
- gdiplusheaders/Font.Font
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Gdiplus.dll
api_name:
- Font.Font
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# Font::Font(IN HDC,IN const LOGFONTA)


## -description


Creates a <b>Font::Font</b> object directly from a Windows Graphics Device Interface (GDI) logical font. The GDI logical font is a 
			<b>LOGFONTA</b> structure, which is the one-byte character version of a logical font. This constructor is provided for compatibility with GDI.


## -parameters




### -param hdc [in]

Type: <b>HDC</b>

Handle to a Windows device context. A handle is a number that Windows uses internally to reference an object. 


### -param logfont [in]

Type: <b>const LOGFONTA*</b>

Pointer to a 
					<b>LOGFONTA</b> structure variable that contains attributes of the font. The 
					<b>LOGFONTA</b> structure is the one-byte character version of the logical font. 


## -remarks



A device context is a structure that is maintained internally. It is associated with a particular device, such as a video monitor or a printer. There is usually one device context associated with each window displayed on a video monitor. A device context contains some graphics attributes used by GDI+.

A 
				<b>LOGFONTA</b> structure is a GDI structure. GDI+ uses only some of the attributes contained in this structure.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-changes-in-the-programming-model-about">Changes in the Programming Model</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font">Font</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-using-text-and-fonts-use">Using Text and Fonts</a>
 

 

