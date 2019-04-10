---
UID: NS:wingdi.tagKERNINGPAIR
title: KERNINGPAIR (wingdi.h)
author: windows-sdk-content
description: The KERNINGPAIR structure defines a kerning pair.
old-location: gdi\kerningpair.htm
tech.root: gdi
ms.assetid: af7bfcf7-467b-4ea9-87c5-3622303b1d8b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPKERNINGPAIR, KERNINGPAIR, KERNINGPAIR structure [Windows GDI], LPKERNINGPAIR, LPKERNINGPAIR structure pointer [Windows GDI], _win32_KERNINGPAIR_str, gdi.kerningpair, wingdi/KERNINGPAIR, wingdi/LPKERNINGPAIR"
ms.topic: struct
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
 - KERNINGPAIR
product: Windows
targetos: Windows
req.typenames: KERNINGPAIR, *LPKERNINGPAIR
req.redist: 
---

# KERNINGPAIR structure


## -description



The <b>KERNINGPAIR</b> structure defines a kerning pair.




## -struct-fields




### -field wFirst

The character code for the first character in the kerning pair.


### -field wSecond

The character code for the second character in the kerning pair.


### -field iKernAmount

The amount this pair will be kerned if they appear side by side in the same font and size. This value is typically negative, because pair kerning usually results in two characters being set more tightly than normal. The value is specified in logical units; that is, it depends on the current mapping mode.


## -see-also




<a href="https://msdn.microsoft.com/93726d5c-d4ed-4681-bf45-cb899f195b5d">Font and Text Structures</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/9aba629f-afab-4ef3-8e1d-d0b90e122e94">GetKerningPairs</a>
 

 

