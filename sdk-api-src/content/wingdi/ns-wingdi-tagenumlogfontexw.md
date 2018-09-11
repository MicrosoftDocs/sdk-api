---
UID: NS:wingdi.tagENUMLOGFONTEXW
title: tagENUMLOGFONTEXW
author: windows-sdk-content
description: The ENUMLOGFONTEX structure contains information about an enumerated font.
old-location: gdi\enumlogfontex.htm
tech.root: gdi
ms.assetid: 2e848e47-5b5f-46ad-9963-55d6bb6748a9
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPENUMLOGFONTEXW, ENUMLOGFONTEX, ENUMLOGFONTEX structure [Windows GDI], ENUMLOGFONTEXA, ENUMLOGFONTEXW, LPENUMLOGFONTEX, LPENUMLOGFONTEX structure pointer [Windows GDI], _win32_ENUMLOGFONTEX_str, gdi.enumlogfontex, tagENUMLOGFONTEXW, wingdi/ENUMLOGFONTEX, wingdi/ENUMLOGFONTEXA, wingdi/ENUMLOGFONTEXW, wingdi/LPENUMLOGFONTEX"
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
---

# tagENUMLOGFONTEXW structure


## -description



The <b>ENUMLOGFONTEX</b> structure contains information about an enumerated font.




## -struct-fields




### -field elfLogFont

A <a href="https://msdn.microsoft.com/57658a03-0a6d-4a28-a7c1-c65ec145beb4">LOGFONT</a> structure that contains values defining the font attributes.


### -field elfFullName

The unique name of the font. For example, ABC Font Company TrueType Bold Italic Sans Serif.


### -field elfStyle

The style of the font. For example, Bold Italic.


### -field elfScript

The script, that is, the character set, of the font. For example, Cyrillic.


## -see-also




<a href="https://msdn.microsoft.com/a4adad4c-ab6a-4adb-a1d3-fea3cfdbaf73">EnumFontFamExProc</a>



<a href="https://msdn.microsoft.com/4d70906d-8005-4c4a-869e-16dd3e6fa3f2">EnumFontFamiliesEx</a>



<a href="https://msdn.microsoft.com/93726d5c-d4ed-4681-bf45-cb899f195b5d">Font and Text Structures</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/57658a03-0a6d-4a28-a7c1-c65ec145beb4">LOGFONT</a>
 

 

