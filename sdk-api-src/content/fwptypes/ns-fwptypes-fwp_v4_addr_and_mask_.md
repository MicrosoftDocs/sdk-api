---
UID: NS:fwptypes.FWP_V4_ADDR_AND_MASK_
title: FWP_V4_ADDR_AND_MASK_
author: windows-sdk-content
description: The FWP_V4_ADDR_AND_MASK structure defines the address and subnet mask for an IPv4 Internet address.
old-location: netvista\fwp_v4_addr_and_mask.htm
tech.root: NetVista
ms.assetid: 3beefa33-1331-4a76-b705-6060a00901f2
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: FWP_V4_ADDR_AND_MASK, FWP_V4_ADDR_AND_MASK structure [Network Drivers Starting with Windows Vista], FWP_V4_ADDR_AND_MASK_, fwptypes/FWP_V4_ADDR_AND_MASK, netvista.fwp_v4_addr_and_mask, wfp_ref_3_struct_1_top_fwp_A-Z_08c85505-84f1-4627-a003-95a1842d544d.xml
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: fwptypes.h
req.include-header: Fwpsk.h
req.target-type: Windows
req.target-min-winverclnt: Available starting with Windows Vista.
req.target-min-winversvr: 
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - fwptypes.h
api_name:
 - FWP_V4_ADDR_AND_MASK
product: Windows
targetos: Windows
req.typenames: FWP_V4_ADDR_AND_MASK
req.redist: 
---

# FWP_V4_ADDR_AND_MASK_ structure


## -description


The FWP_V4_ADDR_AND_MASK structure defines the address and subnet mask for an IPv4 Internet
  address.


## -struct-fields




### -field addr

An IPv4 network address in host byte order.


### -field mask

An IPv4 subnet mask in host byte order.


## -remarks



The FWP_V4_ADDR_AND_MASK structure specifies an IPv4 address and subnet mask as a condition value for
    a filtering condition.




## -see-also




<a href="https://msdn.microsoft.com/8d0aad8c-b224-4066-a10a-7c11ca60a78c">FWP_CONDITION_VALUE0</a>



<a href="https://msdn.microsoft.com/7632d9be-dd16-40d2-b7b4-2d4efb6aaa99">FWP_DATA_TYPE</a>
 

 

