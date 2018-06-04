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

# REGFILTER2 structure


## -description



The <code>REGFILTER2</code> structure contains information for registering a filter.




## -struct-fields




### -field dwVersion

Filter registration format. If the value is 1, the union contains the first unnamed structure. If the value is 2, the union contains the second unnamed structure.


### -field dwMerit

Filter merit. Filters with higher merit are enumerated first. See <a href="https://msdn.microsoft.com/9e026675-e0a9-4c82-9b57-ab0e7d9592ea">Merit</a>.


### -field cPins

Number of pins. (Defined only if <b>dwVersion</b> is 1.)


### -field rgPins

Pointer to an array of <a href="https://msdn.microsoft.com/1da033e1-24c3-46e0-becf-025966e6238f">REGFILTERPINS</a> structures, of size <b>cPins</b>. (Defined only if <b>dwVersion</b> is 1.)


### -field cPins2

Number of pins. (Defined only if <b>dwVersion</b> is 2.)


### -field rgPins2

Pointer to an array of <a href="https://msdn.microsoft.com/a78327f1-a0aa-4e25-b6f8-cf45b92191fa">REGFILTERPINS2</a> structures, of size <b>cPins2</b>. (Defined only if <b>dwVersion</b> is 2.)


## -remarks



This structure is passed to the <a href="https://msdn.microsoft.com/773e527e-2174-4f74-a822-549cfe2927a3">IFilterMapper2::RegisterFilter</a> method.

If you need to register pin mediums or pin categories, set <b>dwVersion</b> to 2 and use the <a href="https://msdn.microsoft.com/a78327f1-a0aa-4e25-b6f8-cf45b92191fa">REGFILTERPINS2</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>
 

 

