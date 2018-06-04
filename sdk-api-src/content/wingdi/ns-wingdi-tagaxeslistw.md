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

# tagAXESLISTW structure


## -description



The <b>AXESLIST</b> structure contains information on all the axes of a multiple master font.




## -struct-fields




### -field axlReserved

Reserved. Must be STAMP_AXESLIST.


### -field axlNumAxes

Number of axes for a specified multiple master font.


### -field axlAxisInfo

An array of <a href="https://msdn.microsoft.com/a947618e-4b50-453a-82d5-5a6f825faebb">AXISINFO</a> structures. Each <b>AXISINFO</b> structure contains information on an axis of a specified multiple master font. This corresponds to the <b>dvValues</b> array in the <a href="https://msdn.microsoft.com/aeff9901-2405-44aa-ba46-8d784afd6b76">DESIGNVECTOR</a> structure.


## -remarks



The PostScript Open Type Font does not support multiple master functionality.

The information on the axes of a multiple master font are specified by the <a href="https://msdn.microsoft.com/a947618e-4b50-453a-82d5-5a6f825faebb">AXISINFO</a> structures. The <b>axlNumAxes</b> member specifies the actual size of <b>axlAxisInfo</b>, while MM_MAX_NUMAXES, which equals 16, is the maximum allowed size of <b>axlAxisInfo</b>.




## -see-also




<a href="https://msdn.microsoft.com/a947618e-4b50-453a-82d5-5a6f825faebb">AXISINFO</a>



<a href="https://msdn.microsoft.com/aeff9901-2405-44aa-ba46-8d784afd6b76">DESIGNVECTOR</a>



<a href="https://msdn.microsoft.com/deb81846-3ada-4c88-8c26-74224538d282">ENUMTEXTMETRIC</a>



<a href="https://msdn.microsoft.com/93726d5c-d4ed-4681-bf45-cb899f195b5d">Font and Text Structures</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>
 

 

