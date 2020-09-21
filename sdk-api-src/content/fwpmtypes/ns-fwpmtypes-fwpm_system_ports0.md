---
UID: NS:fwpmtypes.FWPM_SYSTEM_PORTS0_
title: FWPM_SYSTEM_PORTS0 (fwpmtypes.h)
description: The FWPM_SYSTEM_PORTS0 structure.
helpviewer_keywords: ["FWPM_SYSTEM_PORTS0","FWPM_SYSTEM_PORTS0 structure [Filtering]","fwp.fwpm_system_ports0","fwpmtypes/FWPM_SYSTEM_PORTS0"]
old-location: fwp\fwpm_system_ports0.htm
tech.root: fwp
ms.assetid: cf6fbd43-f603-417d-925d-418d9aec5a03
ms.date: 12/05/2018
ms.keywords: FWPM_SYSTEM_PORTS0, FWPM_SYSTEM_PORTS0 structure [Filtering], fwp.fwpm_system_ports0, fwpmtypes/FWPM_SYSTEM_PORTS0
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
req.typenames: FWPM_SYSTEM_PORTS0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_SYSTEM_PORTS0_
 - fwpmtypes/FWPM_SYSTEM_PORTS0_
 - FWPM_SYSTEM_PORTS0
 - fwpmtypes/FWPM_SYSTEM_PORTS0
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
 - FWPM_SYSTEM_PORTS0
---

# FWPM_SYSTEM_PORTS0 structure


## -description

The <b>FWPM_SYSTEM_PORTS0</b> structure  contains information about all of the system ports of all types.

## -struct-fields

### -field numTypes

The number of types in the array.

### -field types

A [FWPM_SYSTEM_PORTS_BY_TYPE0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_system_ports_by_type0) structure that specifies the array of system port types.

## -remarks

<b>FWPM_SYSTEM_PORTS0</b> is a specific implementation of FWPM_SYSTEM_PORTS. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

[FWPM_SYSTEM_PORTS_BY_TYPE0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_system_ports_by_type0)



<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>