---
UID: NE:oleidl.tagOLECONTF
title: OLECONTF (oleidl.h)
author: windows-sdk-content
description: Indicates the type of objects to be enumerated.
old-location: com\olecontf.htm
tech.root: com
ms.assetid: 9c70fc86-7166-47dd-a424-741f18e381e3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: OLECONTF, OLECONTF enumeration [COM], OLECONTF_EMBEDDINGS, OLECONTF_LINKS, OLECONTF_ONLYIFRUNNING, OLECONTF_ONLYUSER, OLECONTF_OTHERS, _ole_OLECONTF, com.olecontf, oleidl/OLECONTF, oleidl/OLECONTF_EMBEDDINGS, oleidl/OLECONTF_LINKS, oleidl/OLECONTF_ONLYIFRUNNING, oleidl/OLECONTF_ONLYUSER, oleidl/OLECONTF_OTHERS
ms.topic: enum
req.header: oleidl.h
req.include-header: 
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
 - OleIdl.h
api_name:
 - OLECONTF
product: Windows
targetos: Windows
req.typenames: OLECONTF
req.redist: 
---

# OLECONTF enumeration


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
 

 

