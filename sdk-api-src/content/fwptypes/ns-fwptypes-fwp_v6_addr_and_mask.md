---
UID: NS:fwptypes.FWP_V6_ADDR_AND_MASK_
title: FWP_V6_ADDR_AND_MASK (fwptypes.h)
description: Specifies an IPv6 address and mask.
helpviewer_keywords: ["FWP_V6_ADDR_AND_MASK","FWP_V6_ADDR_AND_MASK structure [Filtering]","fwp.fwp_v6_addr_and_mask_struct","fwptypes/FWP_V6_ADDR_AND_MASK"]
old-location: fwp\fwp_v6_addr_and_mask_struct.htm
tech.root: fwp
ms.assetid: d8566d41-677a-424f-89f3-e333a0520288
ms.date: 12/05/2018
ms.keywords: FWP_V6_ADDR_AND_MASK, FWP_V6_ADDR_AND_MASK structure [Filtering], fwp.fwp_v6_addr_and_mask_struct, fwptypes/FWP_V6_ADDR_AND_MASK
req.header: fwptypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: FWP_V6_ADDR_AND_MASK
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWP_V6_ADDR_AND_MASK_
 - fwptypes/FWP_V6_ADDR_AND_MASK_
 - FWP_V6_ADDR_AND_MASK
 - fwptypes/FWP_V6_ADDR_AND_MASK
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
 - FWP_V6_ADDR_AND_MASK
---

# FWP_V6_ADDR_AND_MASK structure


## -description

The <b>FWP_V6_ADDR_AND_MASK</b> structure specifies an IPv6 address and mask.

## -struct-fields

### -field addr

An array of size <b>FWP_V6_ADDR_SIZE</b> bytes containing an IPv6 address. <b>FWP_V6_ADDR_SIZE</b> maps to 16.

### -field prefixLength

Value specifying the prefix length of the IPv6 address.

## -remarks

The mask is specified by the width in bits. For
example, a prefixLength of 16 specifies a mask consisting of 16 1's followed
by 112 0's.

## -see-also

<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>