---
UID: NS:wingdi.tagENUMLOGFONTEXW
title: ENUMLOGFONTEXW (wingdi.h)
author: windows-sdk-content
description: The ENUMLOGFONTEX structure contains information about an enumerated font.
old-location: gdi\enumlogfontex.htm
tech.root: gdi
ms.assetid: 2e848e47-5b5f-46ad-9963-55d6bb6748a9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPENUMLOGFONTEXW, ENUMLOGFONTEX, ENUMLOGFONTEX structure [Windows GDI], ENUMLOGFONTEXA, ENUMLOGFONTEXW, LPENUMLOGFONTEX, LPENUMLOGFONTEX structure pointer [Windows GDI], _win32_ENUMLOGFONTEX_str, gdi.enumlogfontex, wingdi/ENUMLOGFONTEX, wingdi/ENUMLOGFONTEXA, wingdi/ENUMLOGFONTEXW, wingdi/LPENUMLOGFONTEX"
ms.topic: struct
f1_keywords: 
 - "wingdi/ENUMLOGFONTEX"
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ENUMLOGFONTEXW (Unicode) and ENUMLOGFONTEXA (ANSI)
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
 - ENUMLOGFONTEX
 - ENUMLOGFONTEXA
 - ENUMLOGFONTEXW
product: Windows
targetos: Windows
req.typenames: ENUMLOGFONTEXW, *LPENUMLOGFONTEXW
req.redist: 
ms.custom: 19H1
---

# ENUMLOGFONTEXW structure


## -description



The <b>ENUMLOGFONTEX</b> structure contains information about an enumerated font.




## -struct-fields




### -field elfLogFont

A <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-taglogfonta">LOGFONT</a> structure that contains values defining the font attributes.


### -field elfFullName

The unique name of the font. For example, ABC Font Company TrueType Bold Italic Sans Serif.


### -field elfStyle

The style of the font. For example, Bold Italic.


### -field elfScript

The script, that is, the character set, of the font. For example, Cyrillic.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/dd162618(v=vs.85)">EnumFontFamExProc</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-enumfontfamiliesexa">EnumFontFamiliesEx</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/font-and-text-structures">Font and Text Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-taglogfonta">LOGFONT</a>
 

 

