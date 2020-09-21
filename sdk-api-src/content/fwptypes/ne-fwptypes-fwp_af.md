---
UID: NE:fwptypes.FWP_NE_FAMILY_
title: FWP_AF (fwptypes.h)
description: The FWP_AF enumerated type.
helpviewer_keywords: ["FWP_AF","FWP_AF enumeration [Filtering]","FWP_AF_ETHER","FWP_AF_INET","FWP_AF_INET6","FWP_AF_NONE","fwp.fwp_af","fwptypes/FWP_AF","fwptypes/FWP_AF_ETHER","fwptypes/FWP_AF_INET","fwptypes/FWP_AF_INET6","fwptypes/FWP_AF_NONE"]
old-location: fwp\fwp_af.htm
tech.root: fwp
ms.assetid: 358305a6-e0a6-4d01-92be-fd88b3bd32a0
ms.date: 12/05/2018
ms.keywords: FWP_AF, FWP_AF enumeration [Filtering], FWP_AF_ETHER, FWP_AF_INET, FWP_AF_INET6, FWP_AF_NONE, fwp.fwp_af, fwptypes/FWP_AF, fwptypes/FWP_AF_ETHER, fwptypes/FWP_AF_INET, fwptypes/FWP_AF_INET6, fwptypes/FWP_AF_NONE
req.header: fwptypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fwptypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FWP_AF
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWP_NE_FAMILY_
 - fwptypes/FWP_NE_FAMILY_
 - FWP_AF
 - fwptypes/FWP_AF
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fwptypes.h
api_name:
 - FWP_AF
---

# FWP_AF enumeration


## -description

The <b>FWP_AF</b> enumerated type specifies the address family.

## -enum-fields

### -field FWP_AF_INET

Specifies an address as an IPv4 address.

### -field FWP_AF_INET6

Specifies an address as an IPv6 address.

### -field FWP_AF_ETHER

Reserved.

### -field FWP_AF_NONE

Placeholder value to be used when the address family is not yet identified.

## -see-also

[FWP_IP_VERSION](/windows/desktop/api/fwptypes/ne-fwptypes-fwp_ip_version)