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

# tagMKSYS enumeration


## -description


Indicates the moniker's class.


## -enum-fields




### -field MKSYS_NONE

Indicates a custom moniker implementation.


### -field MKSYS_GENERICCOMPOSITE

Indicates the system's generic composite moniker class.


### -field MKSYS_FILEMONIKER

Indicates the system's file moniker class.


### -field MKSYS_ANTIMONIKER

Indicates the system's anti-moniker class.


### -field MKSYS_ITEMMONIKER

Indicates the system's item moniker class.


### -field MKSYS_POINTERMONIKER

Indicates the system's pointer moniker class.


### -field MKSYS_CLASSMONIKER

Indicates the system's class moniker class.


### -field MKSYS_OBJREFMONIKER

Indicates the system's OBJREF moniker class.


### -field MKSYS_SESSIONMONIKER

Indicates the system's terminal server session moniker class.


### -field MKSYS_LUAMONIKER

Indicates the system's elevation moniker class.


## -see-also




<a href="https://msdn.microsoft.com/a61c0df9-786e-45e7-8b3d-f950decc596d">IMoniker::IsSystemMoniker</a>
 

 

