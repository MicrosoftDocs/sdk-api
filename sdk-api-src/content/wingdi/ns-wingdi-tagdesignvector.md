---
UID: NS:wingdi.tagDESIGNVECTOR
title: tagDESIGNVECTOR
author: windows-driver-content
description: The DESIGNVECTOR structure is used by an application to specify values for the axes of a multiple master font.
old-location: gdi\designvector.htm
old-project: gdi
ms.assetid: aeff9901-2405-44aa-ba46-8d784afd6b76
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: "*LPDESIGNVECTOR, *PDESIGNVECTOR, DESIGNVECTOR, DESIGNVECTOR structure [Windows GDI], PDESIGNVECTOR, PDESIGNVECTOR structure pointer [Windows GDI], _win32_DESIGNVECTOR_str, gdi.designvector, tagDESIGNVECTOR, wingdi/DESIGNVECTOR, wingdi/PDESIGNVECTOR"
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
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DESIGNVECTOR, *PDESIGNVECTOR, *LPDESIGNVECTOR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wingdi.h
api_name:
-	DESIGNVECTOR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# tagDESIGNVECTOR structure


## -description



The <b>DESIGNVECTOR</b> structure is used by an application to specify values for the axes of a multiple master font.




## -struct-fields




### -field dvReserved

Reserved. Must be STAMP_DESIGNVECTOR.


### -field dvNumAxes

Number of values in the <b>dvValues</b> array.


### -field dvValues

An array specifying the values of the axes of a multiple master OpenType font. This array corresponds to the <b>axlAxisInfo</b> array in the <a href="https://msdn.microsoft.com/f95f012e-f02b-46c1-94ba-69f426ee7ad9">AXESLIST</a> structure.


## -remarks



The <b>dvNumAxes</b> member determines the actual size of <b>dvValues</b>, and thus, of <b>DESIGNVECTOR</b>. The constant MM_MAX_NUMAXES, which is 16, specifies the maximum allowed size of the <b>dvValues</b> array.

The PostScript Open Type Font does not support multiple master functionality.




## -see-also




<a href="https://msdn.microsoft.com/f95f012e-f02b-46c1-94ba-69f426ee7ad9">AXESLIST</a>



<a href="https://msdn.microsoft.com/ad5153ba-fa9d-4a07-9be3-a07b524c1539">AddFontMemResourceEx</a>



<a href="https://msdn.microsoft.com/eaf8ebf0-1b06-4a09-a842-83540245a117">AddFontResourceEx</a>



<a href="https://msdn.microsoft.com/93726d5c-d4ed-4681-bf45-cb899f195b5d">Font and Text Structures</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/18056fe7-1efe-428e-a828-3217c53371eb">RemoveFontResourceEx</a>
 

 

