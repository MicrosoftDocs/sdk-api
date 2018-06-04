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

# _OMAP structure


## -description


Describes an entry in an address map.


## -struct-fields




### -field rva

A relative virtual address (RVA) in image A.


### -field rvaTo

The relative virtual address that <b>rva</b> is mapped to in image B.


## -remarks



An address map provides a translation from one image layout (A) to another (B). An array of OMAP structures, sorted by <b>rva</b>, defines an address map.

To translate an address, addrA, in image A to an address, addrB, in image B, perform the following steps:

<ol>
<li>Search the map for the entry, e, with the largest rva less than or equal to addrA.</li>
<li>Set delta = addrA – e.rva.</li>
<li>Set addrB = e.rvaTo + delta.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/d89947fa-65fd-4929-9f7e-a4923792049e">SymGetOmaps</a>
 

 

