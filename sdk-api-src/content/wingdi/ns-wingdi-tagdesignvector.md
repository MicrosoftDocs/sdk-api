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
 

 

