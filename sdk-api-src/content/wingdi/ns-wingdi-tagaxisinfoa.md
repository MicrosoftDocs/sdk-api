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

# tagAXISINFOA structure


## -description



The <b>AXISINFO</b> structure contains information about an axis of a multiple master font.




## -struct-fields




### -field axMinValue

The minimum value for this axis.


### -field axMaxValue

The maximum value for this axis.


### -field axAxisName

The name of the axis, specified as an array of characters.


## -remarks



The <b>AXISINFO</b> structure contains the name of an axis in a multiple master font and also the minimum and maximum possible values for the axis. The length of the name is MM_MAX_AXES_NAMELEN, which equals 16. An application queries these values before setting its desired values in the <a href="https://msdn.microsoft.com/aeff9901-2405-44aa-ba46-8d784afd6b76">DESIGNVECTOR</a> array.

The PostScript Open Type Font does not support multiple master functionality.

For the ANSI version of this structure, <b>axAxisName</b> must be an array of bytes.




## -see-also




<a href="https://msdn.microsoft.com/f95f012e-f02b-46c1-94ba-69f426ee7ad9">AXESLIST</a>



<a href="https://msdn.microsoft.com/aeff9901-2405-44aa-ba46-8d784afd6b76">DESIGNVECTOR</a>



<a href="https://msdn.microsoft.com/93726d5c-d4ed-4681-bf45-cb899f195b5d">Font and Text Structures</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>
 

 

