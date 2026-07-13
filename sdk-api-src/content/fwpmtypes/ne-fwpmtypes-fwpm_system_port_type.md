---
UID: NE:fwpmtypes.FWPM_SYSTEM_PORT_TYPE_
title: FWPM_SYSTEM_PORT_TYPE (fwpmtypes.h)
description: The FWPM_SYSTEM_PORT_TYPE enumerated type.
helpviewer_keywords: ["FWPM_SYSTEM_PORT_IPHTTPS_IN","FWPM_SYSTEM_PORT_IPHTTPS_OUT","FWPM_SYSTEM_PORT_RPC_EPMAP","FWPM_SYSTEM_PORT_TEREDO","FWPM_SYSTEM_PORT_TYPE","FWPM_SYSTEM_PORT_TYPE enumeration [Filtering]","FWPM_SYSTEM_PORT_TYPE_MAX","fwp.fwpm_system_port_type","fwpmtypes/FWPM_SYSTEM_PORT_IPHTTPS_IN","fwpmtypes/FWPM_SYSTEM_PORT_IPHTTPS_OUT","fwpmtypes/FWPM_SYSTEM_PORT_RPC_EPMAP","fwpmtypes/FWPM_SYSTEM_PORT_TEREDO","fwpmtypes/FWPM_SYSTEM_PORT_TYPE","fwpmtypes/FWPM_SYSTEM_PORT_TYPE_MAX"]
old-location: fwp\fwpm_system_port_type.htm
tech.root: fwp
ms.assetid: 7e4fbcbd-a8c5-4ae5-ba69-46d8e7cbcbc9
ms.date: 12/05/2018
ms.keywords: FWPM_SYSTEM_PORT_IPHTTPS_IN, FWPM_SYSTEM_PORT_IPHTTPS_OUT, FWPM_SYSTEM_PORT_RPC_EPMAP, FWPM_SYSTEM_PORT_TEREDO, FWPM_SYSTEM_PORT_TYPE, FWPM_SYSTEM_PORT_TYPE enumeration [Filtering], FWPM_SYSTEM_PORT_TYPE_MAX, fwp.fwpm_system_port_type, fwpmtypes/FWPM_SYSTEM_PORT_IPHTTPS_IN, fwpmtypes/FWPM_SYSTEM_PORT_IPHTTPS_OUT, fwpmtypes/FWPM_SYSTEM_PORT_RPC_EPMAP, fwpmtypes/FWPM_SYSTEM_PORT_TEREDO, fwpmtypes/FWPM_SYSTEM_PORT_TYPE, fwpmtypes/FWPM_SYSTEM_PORT_TYPE_MAX
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
req.typenames: FWPM_SYSTEM_PORT_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_SYSTEM_PORT_TYPE_
 - fwpmtypes/FWPM_SYSTEM_PORT_TYPE_
 - FWPM_SYSTEM_PORT_TYPE
 - fwpmtypes/FWPM_SYSTEM_PORT_TYPE
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
 - FWPM_SYSTEM_PORT_TYPE
---

# FWPM_SYSTEM_PORT_TYPE enumeration


## -description

The <b>FWPM_SYSTEM_PORT_TYPE</b> enumerated type specifies the type of system port.

## -enum-fields

### -field FWPM_SYSTEM_PORT_RPC_EPMAP:0

Specifies a system port used by an RPC endpoint mapper.

### -field FWPM_SYSTEM_PORT_TEREDO

Specifies a system port used by the Teredo service.

### -field FWPM_SYSTEM_PORT_IPHTTPS_IN

Specifies an inbound system port used by the IP in conjunction with HTTPS implementation.

### -field FWPM_SYSTEM_PORT_IPHTTPS_OUT

Specifies an outbound system port used by the IP in conjunction with HTTPS implementation.

### -field FWPM_SYSTEM_PORT_TYPE_MAX

Maximum value for testing purposes.

## -see-also

<a href="/windows/desktop/FWP/fwp-enums">Windows Filtering Platform API Enumerated Types</a>
