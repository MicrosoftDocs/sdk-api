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

# REGFILTERPINS2 structure


## -description



The <code>REGFILTERPINS2</code> structure contains information for registering a filter through the <a href="https://msdn.microsoft.com/6a3db838-cee3-4a9f-a924-fb55931acc83">IFilterMapper2</a> interface.




## -struct-fields




### -field dwFlags

Bitwise combination of zero or more <a href="https://msdn.microsoft.com/85d9f9b6-229f-41ea-87bb-097af591c2d2">REG_PINFLAG</a> flags.


### -field cInstances

Number of instances of this pin.


### -field nMediaTypes

Number of media types supported by this pin.


### -field lpMediaType

Pointer to an array of <a href="https://msdn.microsoft.com/aa31f856-4151-420d-a69d-34ef3a105130">REGPINTYPES</a> structures, of size nMediaTypes.


### -field nMediums

Number of mediums. Can be zero.


### -field lpMedium

Pointer to an array of <a href="https://msdn.microsoft.com/ed5614fe-bfeb-4ddf-a626-b14080f45b33">REGPINMEDIUM</a> structures, of size nMediums.


### -field clsPinCategory

Optional pin category, from the <a href="https://msdn.microsoft.com/0c01bd51-353d-4f48-b33c-796f740915e2">Pin Property Set</a>.


## -remarks



If you use this structure, set the <b>dwVersion</b> member of the <a href="https://msdn.microsoft.com/651b94e6-b343-4957-9781-768b04c098dd">REGFILTER2</a> structure to 2.




## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>
 

 

