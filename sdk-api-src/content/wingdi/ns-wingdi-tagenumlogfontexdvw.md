---
UID: NS:wingdi.tagENUMLOGFONTEXDVW
title: tagENUMLOGFONTEXDVW
author: windows-sdk-content
description: The ENUMLOGFONTEXDV structure contains the information used to create a font.
old-location: gdi\enumlogfontexdv.htm
tech.root: gdi
ms.assetid: 8d483f52-250e-4c4f-83cf-ff952bb84fd3
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: "*LPENUMLOGFONTEXDVW, *PENUMLOGFONTEXDVW, ENUMLOGFONTEXDV, ENUMLOGFONTEXDV structure [Windows GDI], ENUMLOGFONTEXDVA, ENUMLOGFONTEXDVW, PENUMLOGFONTEXDV, PENUMLOGFONTEXDV structure pointer [Windows GDI], _win32_ENUMLOGFONTEXDV_str, gdi.enumlogfontexdv, tagENUMLOGFONTEXDVW, wingdi/ENUMLOGFONTEXDV, wingdi/ENUMLOGFONTEXDVA, wingdi/ENUMLOGFONTEXDVW, wingdi/PENUMLOGFONTEXDV"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ENUMLOGFONTEXDVW (Unicode) and ENUMLOGFONTEXDVA (ANSI)
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
 - ENUMLOGFONTEXDV
 - ENUMLOGFONTEXDVA
 - ENUMLOGFONTEXDVW
product: Windows
targetos: Windows
req.typenames: ENUMLOGFONTEXDVW, *PENUMLOGFONTEXDVW, *LPENUMLOGFONTEXDVW
req.redist: 
---

# tagENUMLOGFONTEXDVW structure


## -description



The <b>ENUMLOGFONTEXDV</b> structure contains the information used to create a font.




## -struct-fields




### -field elfEnumLogfontEx

An <a href="https://msdn.microsoft.com/2e848e47-5b5f-46ad-9963-55d6bb6748a9">ENUMLOGFONTEX</a> structure that contains information about the logical attributes of the font.


### -field elfDesignVector

A <a href="https://msdn.microsoft.com/aeff9901-2405-44aa-ba46-8d784afd6b76">DESIGNVECTOR</a> structure. This is zero-filled unless the font described is a multiple master OpenType font.


## -remarks



The actual size of <b>ENUMLOGFONTEXDV</b> depends on that of <a href="https://msdn.microsoft.com/aeff9901-2405-44aa-ba46-8d784afd6b76">DESIGNVECTOR</a>, which, in turn depends on its <b>dvNumAxes</b> member.

The <a href="https://msdn.microsoft.com/b5dfc38d-c400-4900-a15b-f251815ee346">EnumFonts</a>, <a href="https://msdn.microsoft.com/4960afbb-eeba-4030-ac89-d1ff077bb2f3">EnumFontFamilies</a>, and <a href="https://msdn.microsoft.com/4d70906d-8005-4c4a-869e-16dd3e6fa3f2">EnumFontFamiliesEx</a> functions have been modified to return pointers to <a href="https://msdn.microsoft.com/deb81846-3ada-4c88-8c26-74224538d282">ENUMTEXTMETRIC</a> and <b>ENUMLOGFONTEXDV</b> to the callback function.




## -see-also




<a href="https://msdn.microsoft.com/1161b79e-f9c8-4073-97c4-1ccc1a78279b">CreateFontIndirectEx</a>



<a href="https://msdn.microsoft.com/aeff9901-2405-44aa-ba46-8d784afd6b76">DESIGNVECTOR</a>



<a href="https://msdn.microsoft.com/deb81846-3ada-4c88-8c26-74224538d282">ENUMTEXTMETRIC</a>



<a href="https://msdn.microsoft.com/4960afbb-eeba-4030-ac89-d1ff077bb2f3">EnumFontFamilies</a>



<a href="https://msdn.microsoft.com/4d70906d-8005-4c4a-869e-16dd3e6fa3f2">EnumFontFamiliesEx</a>



<a href="https://msdn.microsoft.com/b5dfc38d-c400-4900-a15b-f251815ee346">EnumFonts</a>



<a href="https://msdn.microsoft.com/93726d5c-d4ed-4681-bf45-cb899f195b5d">Font and Text Structures</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>
 

 

