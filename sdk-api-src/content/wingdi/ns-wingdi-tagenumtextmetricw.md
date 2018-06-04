---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# tagENUMTEXTMETRICW structure


## -description



The <b>ENUMTEXTMETRIC</b> structure contains information about a physical font.




## -struct-fields




### -field etmNewTextMetricEx

A <a href="https://msdn.microsoft.com/b85ff705-2dd4-4877-9905-d4c2a0894e24">NEWTEXTMETRICEX</a> structure, containing information about a physical font.


### -field etmAxesList

An <a href="https://msdn.microsoft.com/f95f012e-f02b-46c1-94ba-69f426ee7ad9">AXESLIST</a> structure, containing information about the axes for the font. This is only used for multiple master fonts.


## -remarks



<b>ENUMTEXTMETRIC</b> is an extension of <a href="https://msdn.microsoft.com/b85ff705-2dd4-4877-9905-d4c2a0894e24">NEWTEXTMETRICEX</a> that includes the axis information for a multiple master font.


         The <a href="https://msdn.microsoft.com/b5dfc38d-c400-4900-a15b-f251815ee346">EnumFonts</a>, <a href="https://msdn.microsoft.com/4960afbb-eeba-4030-ac89-d1ff077bb2f3">EnumFontFamilies</a>, and <a href="https://msdn.microsoft.com/4d70906d-8005-4c4a-869e-16dd3e6fa3f2">EnumFontFamiliesEx</a> functions have been modified to return pointers to the <b>ENUMTEXTMETRIC</b> and <a href="https://msdn.microsoft.com/8d483f52-250e-4c4f-83cf-ff952bb84fd3">ENUMLOGFONTEXDV</a> structures.




## -see-also




<a href="https://msdn.microsoft.com/f95f012e-f02b-46c1-94ba-69f426ee7ad9">AXESLIST</a>



<a href="https://msdn.microsoft.com/2e848e47-5b5f-46ad-9963-55d6bb6748a9">ENUMLOGFONTEX</a>



<a href="https://msdn.microsoft.com/8d483f52-250e-4c4f-83cf-ff952bb84fd3">ENUMLOGFONTEXDV</a>



<a href="https://msdn.microsoft.com/deb81846-3ada-4c88-8c26-74224538d282">ENUMTEXTMETRIC</a>



<a href="https://msdn.microsoft.com/4960afbb-eeba-4030-ac89-d1ff077bb2f3">EnumFontFamilies</a>



<a href="https://msdn.microsoft.com/4d70906d-8005-4c4a-869e-16dd3e6fa3f2">EnumFontFamiliesEx</a>



<a href="https://msdn.microsoft.com/b5dfc38d-c400-4900-a15b-f251815ee346">EnumFonts</a>



<a href="https://msdn.microsoft.com/93726d5c-d4ed-4681-bf45-cb899f195b5d">Font and Text Structures</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/b85ff705-2dd4-4877-9905-d4c2a0894e24">NEWTEXTMETRICEX</a>
 

 

