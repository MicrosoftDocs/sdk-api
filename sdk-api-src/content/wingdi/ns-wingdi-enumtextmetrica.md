---
UID: NS:wingdi.tagENUMTEXTMETRICA
title: ENUMTEXTMETRICA (wingdi.h)
description: The ENUMTEXTMETRIC structure contains information about a physical font.helpviewer_keywords: ["*LPENUMTEXTMETRICA","*PENUMTEXTMETRICA","ENUMTEXTMETRIC","ENUMTEXTMETRIC structure [Windows GDI]","ENUMTEXTMETRICA","ENUMTEXTMETRICW","PENUMTEXTMETRIC","PENUMTEXTMETRIC structure pointer [Windows GDI]","_win32_ENUMTEXTMETRIC_str","gdi.enumtextmetric","wingdi/ENUMTEXTMETRIC","wingdi/ENUMTEXTMETRICA","wingdi/ENUMTEXTMETRICW","wingdi/PENUMTEXTMETRIC"]
old-location: gdi\enumtextmetric.htm
tech.root: gdi
ms.assetid: deb81846-3ada-4c88-8c26-74224538d282
ms.date: 12/05/2018
ms.keywords: '*LPENUMTEXTMETRICA, *PENUMTEXTMETRICA, ENUMTEXTMETRIC, ENUMTEXTMETRIC structure [Windows GDI], ENUMTEXTMETRICA, ENUMTEXTMETRICW, PENUMTEXTMETRIC, PENUMTEXTMETRIC structure pointer [Windows GDI], _win32_ENUMTEXTMETRIC_str, gdi.enumtextmetric, wingdi/ENUMTEXTMETRIC, wingdi/ENUMTEXTMETRICA, wingdi/ENUMTEXTMETRICW, wingdi/PENUMTEXTMETRIC'
f1_keywords:
- wingdi/ENUMTEXTMETRIC
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
req.unicode-ansi: ENUMTEXTMETRICW (Unicode) and ENUMTEXTMETRICA (ANSI)
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
- ENUMTEXTMETRIC
- ENUMTEXTMETRICA
- ENUMTEXTMETRICW
targetos: Windows
req.typenames: ENUMTEXTMETRICA, *PENUMTEXTMETRICA, *LPENUMTEXTMETRICA
req.redist: 
ms.custom: 19H1
---

# ENUMTEXTMETRICA structure


## -description



The <b>ENUMTEXTMETRIC</b> structure contains information about a physical font.




## -struct-fields




### -field etmNewTextMetricEx

A <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-newtextmetricexa">NEWTEXTMETRICEX</a> structure, containing information about a physical font.


### -field etmAxesList

An <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-axeslista">AXESLIST</a> structure, containing information about the axes for the font. This is only used for multiple master fonts.


## -remarks



<b>ENUMTEXTMETRIC</b> is an extension of <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-newtextmetricexa">NEWTEXTMETRICEX</a> that includes the axis information for a multiple master font.

The <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-enumfontsa">EnumFonts</a>, <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-enumfontfamiliesa">EnumFontFamilies</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-enumfontfamiliesexa">EnumFontFamiliesEx</a> functions have been modified to return pointers to the <b>ENUMTEXTMETRIC</b> and <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-enumlogfontexdva">ENUMLOGFONTEXDV</a> structures.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-axeslista">AXESLIST</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-enumlogfontexa">ENUMLOGFONTEX</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-enumlogfontexdva">ENUMLOGFONTEXDV</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-enumtextmetrica">ENUMTEXTMETRIC</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-enumfontfamiliesa">EnumFontFamilies</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-enumfontfamiliesexa">EnumFontFamiliesEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-enumfontsa">EnumFonts</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/font-and-text-structures">Font and Text Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-newtextmetricexa">NEWTEXTMETRICEX</a>
 

 

