---
UID: NS:fwptypes.FWP_V6_ADDR_AND_MASK_
title: FWP_V6_ADDR_AND_MASK_
author: windows-sdk-content
description: Specifies an IPv6 address and mask.
old-location: fwp\fwp_v6_addr_and_mask_struct.htm
tech.root: fwp
ms.assetid: d8566d41-677a-424f-89f3-e333a0520288
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: FWP_V6_ADDR_AND_MASK, FWP_V6_ADDR_AND_MASK structure [Filtering], FWP_V6_ADDR_AND_MASK_, fwp.fwp_v6_addr_and_mask_struct, fwptypes/FWP_V6_ADDR_AND_MASK
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fwptypes.h
api_name:
 - FWP_V6_ADDR_AND_MASK
product: Windows
targetos: Windows
req.typenames: FWP_V6_ADDR_AND_MASK
req.redist: 
---

# FWP_V6_ADDR_AND_MASK_ structure


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




<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

