---
UID: NS:wingdi.tagENUMLOGFONTW
title: tagENUMLOGFONTW
author: windows-sdk-content
description: The ENUMLOGFONT structure defines the attributes of a font, the complete name of a font, and the style of a font.
old-location: gdi\enumlogfont.htm
old-project: gdi
ms.assetid: cfae9e97-c714-40fb-88ab-95e12ea3ffa9
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: "*LPENUMLOGFONTW, ENUMLOGFONT, ENUMLOGFONT structure [Windows GDI], ENUMLOGFONTA, ENUMLOGFONTW, LPENUMLOGFONT, LPENUMLOGFONT structure pointer [Windows GDI], _win32_ENUMLOGFONT_str, gdi.enumlogfont, tagENUMLOGFONTW, wingdi/ENUMLOGFONT, wingdi/ENUMLOGFONTA, wingdi/ENUMLOGFONTW, wingdi/LPENUMLOGFONT"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ENUMLOGFONTW (Unicode) and ENUMLOGFONTA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: ENUMLOGFONTW, *LPENUMLOGFONTW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - ENUMLOGFONT
 - ENUMLOGFONTA
 - ENUMLOGFONTW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# tagENUMLOGFONTW structure


## -description



The <b>ENUMLOGFONT</b> structure defines the attributes of a font, the complete name of a font, and the style of a font.




## -struct-fields




### -field elfLogFont

A <a href="https://msdn.microsoft.com/57658a03-0a6d-4a28-a7c1-c65ec145beb4">LOGFONT</a> structure that defines the attributes of a font.


### -field elfFullName

A unique name for the font. For example, ABCD Font Company TrueType Bold Italic Sans Serif.


### -field elfStyle

The style of the font. For example, Bold Italic.


## -see-also




<a href="https://msdn.microsoft.com/9957885a-abf7-4d7c-ae8d-40f5d1150591">EnumFontFamProc</a>



<a href="https://msdn.microsoft.com/93726d5c-d4ed-4681-bf45-cb899f195b5d">Font and Text Structures</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/57658a03-0a6d-4a28-a7c1-c65ec145beb4">LOGFONT</a>
 

 

