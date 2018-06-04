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

# tagOLECONTF enumeration


## -description


Indicates the type of objects 
    to be enumerated.


## -enum-fields




### -field OLECONTF_EMBEDDINGS

Enumerates the embedded objects in the container.


### -field OLECONTF_LINKS

Enumerates the linked objects in the container.


### -field OLECONTF_OTHERS

Enumerates all objects in the container that are not OLE compound document objects (i.e., objects other than 
       linked or embedded objects). Use this flag to enumerate the container's pseudo-objects.


### -field OLECONTF_ONLYUSER

Enumerates only those objects the user is aware of. For example, hidden named-ranges in Microsoft Excel would 
       not be enumerated using this value.


### -field OLECONTF_ONLYIFRUNNING

Enumerates only those linked or embedded objects that are currently in the running state for this 
       container.


## -see-also




<a href="https://msdn.microsoft.com/5aaed96f-39c1-4201-80d0-a2a8a177b65e">IEnumUnknown</a>



<a href="https://msdn.microsoft.com/7d825c71-506c-4fd3-ab48-6006f2858d05">IOleContainer::EnumObjects</a>



<a href="https://msdn.microsoft.com/4ae01518-8762-4bce-ad9c-4dc2635e743d">IVBGetControl::EnumControls</a>
 

 

