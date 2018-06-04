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

# FWPM_SYSTEM_PORTS_BY_TYPE0_ structure


## -description


The <b>FWPM_SYSTEM_PORTS_BY_TYPE0</b> structure  contains information about the system ports of a specified type.


## -struct-fields




### -field type

An <a href="https://msdn.microsoft.com/7e4fbcbd-a8c5-4ae5-ba69-46d8e7cbcbc9">FWPM_SYSTEM_PORT_TYPE</a> enumeration that specifies the type of port.


### -field numPorts

The number of ports of the specified type.


### -field ports

Array of IP port numbers for the specified type.


## -remarks



<b>FWPM_SYSTEM_PORTS_BY_TYPE0</b> is a specific implementation of FWPM_SYSTEM_PORTS_BY_TYPE. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/7e4fbcbd-a8c5-4ae5-ba69-46d8e7cbcbc9">FWPM_SYSTEM_PORT_TYPE</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

