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

# MFTOPOLOGY_HARDWARE_MODE enumeration


## -description


Specifies whether the topology loader will insert hardware-based Media Foundation transforms (MFTs) into the topology.


## -enum-fields




### -field MFTOPOLOGY_HWMODE_SOFTWARE_ONLY

Use only software  MFTs. Do not use hardware-based MFTs. This mode is the default, for backward compatibility with existing applications.


### -field MFTOPOLOGY_HWMODE_USE_HARDWARE

Use hardware-based MFTs when possible, and software MFTs otherwise. This mode is the recommended one.


### -field MFTOPOLOGY_HWMODE_USE_ONLY_HARDWARE

If hardware-based MFTs are available, the topoloader will insert
    them.  If not, the connection will fail.

Supported in Windows 8.1 and later.


## -remarks




        This enumeration is used with the <a href="https://msdn.microsoft.com/f7ac3c9b-c163-412f-84c0-27bf551091d8">MF_TOPOLOGY_HARDWARE_MODE</a> topology attribute.
      




## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

