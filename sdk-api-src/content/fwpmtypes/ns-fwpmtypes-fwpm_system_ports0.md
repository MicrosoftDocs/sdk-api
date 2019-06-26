---
UID: NS:fwpmtypes.FWPM_SYSTEM_PORTS0_
title: FWPM_SYSTEM_PORTS0 (fwpmtypes.h)
author: windows-sdk-content
description: The FWPM_SYSTEM_PORTS0 structure.
old-location: fwp\fwpm_system_ports0.htm
tech.root: fwp
ms.assetid: cf6fbd43-f603-417d-925d-418d9aec5a03
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FWPM_SYSTEM_PORTS0, FWPM_SYSTEM_PORTS0 structure [Filtering], fwp.fwpm_system_ports0, fwpmtypes/FWPM_SYSTEM_PORTS0
ms.topic: struct
f1_keywords: 
 - "fwpmtypes/FWPM_SYSTEM_PORTS0"
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
ms.custom: 19H1
---

# FWPM_SYSTEM_PORTS0 structure


## -description


The <b>FWPM_SYSTEM_PORTS0</b> structure  contains information about all of the system ports of all types.


## -struct-fields




### -field numTypes

The number of types in the array.


### -field types

A <a href="https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_system_ports_by_type0_">FWPM_SYSTEM_PORTS_BY_TYPE0</a> structure that specifies the array of system port types.


## -remarks



<b>FWPM_SYSTEM_PORTS0</b> is a specific implementation of FWPM_SYSTEM_PORTS. See <a href="https://docs.microsoft.com/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_system_ports_by_type0_">FWPM_SYSTEM_PORTS_BY_TYPE0</a>



<a href="https://docs.microsoft.com/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
 

 

