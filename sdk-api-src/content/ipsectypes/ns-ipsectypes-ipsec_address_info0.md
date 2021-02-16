---
UID: NS:ipsectypes.IPSEC_ADDRESS_INFO0_
title: IPSEC_ADDRESS_INFO0 (ipsectypes.h)
description: Is used to store mobile additional address information.
helpviewer_keywords: ["IPSEC_ADDRESS_INFO0","IPSEC_ADDRESS_INFO0 structure [Filtering]","fwp.ipsec_address_info0","ipsectypes/IPSEC_ADDRESS_INFO0"]
old-location: fwp\ipsec_address_info0.htm
tech.root: fwp
ms.assetid: ad6a271f-6513-44ac-aa9a-14811b32a06b
ms.date: 12/05/2018
ms.keywords: IPSEC_ADDRESS_INFO0, IPSEC_ADDRESS_INFO0 structure [Filtering], fwp.ipsec_address_info0, ipsectypes/IPSEC_ADDRESS_INFO0
req.header: ipsectypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ipsectypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: IPSEC_ADDRESS_INFO0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPSEC_ADDRESS_INFO0_
 - ipsectypes/IPSEC_ADDRESS_INFO0_
 - IPSEC_ADDRESS_INFO0
 - ipsectypes/IPSEC_ADDRESS_INFO0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ipsectypes.h
api_name:
 - IPSEC_ADDRESS_INFO0
---

# IPSEC_ADDRESS_INFO0 structure


## -description

The <b>IPSEC_ADDRESS_INFO0</b> structure is used to store mobile additional address information.

## -struct-fields

### -field numV4Addresses

The number of IPv4 addresses stored in the <b>v4Addresses</b> member.

### -field v4Addresses

Array of IPv4 local addresses to indicate to peer.

### -field numV6Addresses

The number of IPv6 addresses stored in the <b>v6Addresses</b> member.

### -field v6Addresses

Array of IPv6 local addresses to indicate to peer.

## -remarks

<b>IPSEC_ADDRESS_INFO0</b> is a specific implementation of IPSEC_ADDRESS_INFO. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>