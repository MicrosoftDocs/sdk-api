---
UID: NS:fwpmtypes.FWPM_SYSTEM_PORTS_BY_TYPE0_
title: FWPM_SYSTEM_PORTS_BY_TYPE0 (fwpmtypes.h)
description: The FWPM_SYSTEM_PORTS_BY_TYPE0 structure.
helpviewer_keywords: ["FWPM_SYSTEM_PORTS_BY_TYPE0","FWPM_SYSTEM_PORTS_BY_TYPE0 structure [Filtering]","fwp.fwpm_system_ports_by_type0","fwpmtypes/FWPM_SYSTEM_PORTS_BY_TYPE0"]
old-location: fwp\fwpm_system_ports_by_type0.htm
tech.root: fwp
ms.assetid: 9a1d5431-fe83-468e-bc0e-8e55342ae205
ms.date: 12/05/2018
ms.keywords: FWPM_SYSTEM_PORTS_BY_TYPE0, FWPM_SYSTEM_PORTS_BY_TYPE0 structure [Filtering], fwp.fwpm_system_ports_by_type0, fwpmtypes/FWPM_SYSTEM_PORTS_BY_TYPE0
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
targetos: Windows
req.typenames: FWPM_SYSTEM_PORTS_BY_TYPE0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_SYSTEM_PORTS_BY_TYPE0_
 - fwpmtypes/FWPM_SYSTEM_PORTS_BY_TYPE0_
 - FWPM_SYSTEM_PORTS_BY_TYPE0
 - fwpmtypes/FWPM_SYSTEM_PORTS_BY_TYPE0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fwpmtypes.h
api_name:
 - FWPM_SYSTEM_PORTS_BY_TYPE0
---

# FWPM_SYSTEM_PORTS_BY_TYPE0 structure


## -description

The <b>FWPM_SYSTEM_PORTS_BY_TYPE0</b> structure  contains information about the system ports of a specified type.

## -struct-fields

### -field type

An [FWPM_SYSTEM_PORT_TYPE](/windows/desktop/api/fwpmtypes/ne-fwpmtypes-fwpm_system_port_type) enumeration that specifies the type of port.

### -field numPorts

The number of ports of the specified type.

### -field ports

Array of IP port numbers for the specified type.

## -remarks

<b>FWPM_SYSTEM_PORTS_BY_TYPE0</b> is a specific implementation of FWPM_SYSTEM_PORTS_BY_TYPE. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

[FWPM_SYSTEM_PORT_TYPE](/windows/desktop/api/fwpmtypes/ne-fwpmtypes-fwpm_system_port_type)



<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>