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

# _VM_GENCOUNTER structure


## -description


Describes a virtual machine generation identifier.


## -struct-fields




### -field GenerationCount

The low 64 bits of the virtual machine generation identifier. 


### -field GenerationCountHigh

The high 64 bits of the virtual machine generation identifier. 


## -remarks



For info about the virtual machine generation identifier, see <a href="https://msdn.microsoft.com/0793E46B-8464-425E-8C5B-77C14DA90004">Virtual machine generation identifier</a>.




## -see-also




<a href="https://msdn.microsoft.com/D8945F17-8982-4694-BDD9-DD67963626D1">IOCTL_VMGENCOUNTER_READ</a>
 

 

