---
UID: NC:fwpmu.FWPM_SYSTEM_PORTS_CALLBACK0
title: FWPM_SYSTEM_PORTS_CALLBACK0 (fwpmu.h)
description: Is used to add custom behavior to the system port subscription process.
helpviewer_keywords: ["FWPM_SYSTEM_PORTS_CALLBACK0","FWPM_SYSTEM_PORTS_CALLBACK0 callback","FWPM_SYSTEM_PORTS_CALLBACK0 callback function [Filtering]","fwp.fwpm_system_ports_callback0_func","fwpmu/FWPM_SYSTEM_PORTS_CALLBACK0"]
old-location: fwp\fwpm_system_ports_callback0_func.htm
tech.root: fwp
ms.assetid: 91bf0d89-f760-4de9-8e9b-ece93b6c84ae
ms.date: 12/05/2018
ms.keywords: FWPM_SYSTEM_PORTS_CALLBACK0, FWPM_SYSTEM_PORTS_CALLBACK0 callback, FWPM_SYSTEM_PORTS_CALLBACK0 callback function [Filtering], fwp.fwpm_system_ports_callback0_func, fwpmu/FWPM_SYSTEM_PORTS_CALLBACK0
req.header: fwpmu.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_SYSTEM_PORTS_CALLBACK0
 - fwpmu/FWPM_SYSTEM_PORTS_CALLBACK0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Fwpmu.h
api_name:
 - FWPM_SYSTEM_PORTS_CALLBACK0
---

# FWPM_SYSTEM_PORTS_CALLBACK0 callback function


## -description

The <b>FWPM_SYSTEM_PORTS_CALLBACK0</b> function is used to add custom behavior to the system port subscription process.

## -parameters

### -param context [in, out]

Type: <b>void*</b>

Optional context pointer. It contains the value of the <i>context</i> parameter of the <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmsystemportssubscribe0">FwpmSystemPortsSubscribe0</a> function.

### -param sysPorts [in]

Type: [FWPM_SYSTEM_PORTS0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_system_ports0)*</b>

The system port information.

## -remarks

Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmsystemportssubscribe0">FwpmSystemPortsSubscribe0</a> to register this callback function.

<b>FWPM_SYSTEM_PORTS_CALLBACK0</b> is a specific implementation of FWPM_SYSTEM_PORTS_CALLBACK. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

[FWPM_SYSTEM_PORTS0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_system_ports0)



<a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmsystemportssubscribe0">FwpmSystemPortsSubscribe0</a>
