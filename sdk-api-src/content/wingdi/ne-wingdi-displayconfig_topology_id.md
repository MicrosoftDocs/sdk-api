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

# DISPLAYCONFIG_TOPOLOGY_ID enumeration


## -description


The DISPLAYCONFIG_TOPOLOGY_ID enumeration specifies the type of display topology.


## -enum-fields




### -field DISPLAYCONFIG_TOPOLOGY_INTERNAL

Indicates that the display topology is an internal configuration. 


### -field DISPLAYCONFIG_TOPOLOGY_CLONE

Indicates that the display topology is clone-view configuration. 


### -field DISPLAYCONFIG_TOPOLOGY_EXTEND

Indicates that the display topology is an extended configuration. 


### -field DISPLAYCONFIG_TOPOLOGY_EXTERNAL

Indicates that the display topology is an external configuration. 


### -field DISPLAYCONFIG_TOPOLOGY_FORCE_UINT32

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. You should not use this value. 

