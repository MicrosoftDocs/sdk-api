---
UID: NS:fwpmtypes.FWPM_SYSTEM_PORTS0_
title: FWPM_SYSTEM_PORTS0_
author: windows-sdk-content
description: The FWPM_SYSTEM_PORTS0 structure.
old-location: fwp\fwpm_system_ports0.htm
tech.root: FWP
ms.assetid: cf6fbd43-f603-417d-925d-418d9aec5a03
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: FWPM_SYSTEM_PORTS0, FWPM_SYSTEM_PORTS0 structure [Filtering], FWPM_SYSTEM_PORTS0_, fwp.fwpm_system_ports0, fwpmtypes/FWPM_SYSTEM_PORTS0
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
 - FWPM_SYSTEM_PORTS0
product: Windows
targetos: Windows
req.typenames: FWPM_SYSTEM_PORTS0
req.redist: 
---

# FWPM_SYSTEM_PORTS0_ structure


## -description


The <b>FWPM_SYSTEM_PORTS0</b> structure  contains information about all of the system ports of all types.


## -struct-fields




### -field numTypes

The number of types in the array.


### -field types

A <a href="https://msdn.microsoft.com/9a1d5431-fe83-468e-bc0e-8e55342ae205">FWPM_SYSTEM_PORTS_BY_TYPE0</a> structure that specifies the array of system port types.


## -remarks



<b>FWPM_SYSTEM_PORTS0</b> is a specific implementation of FWPM_SYSTEM_PORTS. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/9a1d5431-fe83-468e-bc0e-8e55342ae205">FWPM_SYSTEM_PORTS_BY_TYPE0</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

