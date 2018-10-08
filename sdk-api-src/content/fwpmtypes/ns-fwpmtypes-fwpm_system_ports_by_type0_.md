---
UID: NS:fwpmtypes.FWPM_SYSTEM_PORTS_BY_TYPE0_
title: FWPM_SYSTEM_PORTS_BY_TYPE0_
author: windows-sdk-content
description: The FWPM_SYSTEM_PORTS_BY_TYPE0 structure.
old-location: fwp\fwpm_system_ports_by_type0.htm
tech.root: fwp
ms.assetid: 9a1d5431-fe83-468e-bc0e-8e55342ae205
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: FWPM_SYSTEM_PORTS_BY_TYPE0, FWPM_SYSTEM_PORTS_BY_TYPE0 structure [Filtering], FWPM_SYSTEM_PORTS_BY_TYPE0_, fwp.fwpm_system_ports_by_type0, fwpmtypes/FWPM_SYSTEM_PORTS_BY_TYPE0
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fwpmtypes.idl
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
 - Fwpmtypes.h
api_name:
 - FWPM_SYSTEM_PORTS_BY_TYPE0
product: Windows
targetos: Windows
req.typenames: FWPM_SYSTEM_PORTS_BY_TYPE0
req.redist: 
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
 

 

