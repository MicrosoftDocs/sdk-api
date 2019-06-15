---
UID: NF:rtmv2.RTM_IPV4_SET_ADDR_AND_MASK
title: RTM_IPV4_SET_ADDR_AND_MASK macro (rtmv2.h)
author: windows-sdk-content
description: The RTM_IPV4_SET_ADDR_AND_MASK macro converts an IPv4 address and mask to a generic RTM_NET_ADDRESS structure.
old-location: rras\rtm_ipv4_set_addr_and_mask.htm
tech.root: RRAS
ms.assetid: 23849eed-309a-41b8-b853-1267806166fa
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RTM_IPV4_SET_ADDR_AND_MASK, RTM_IPV4_SET_ADDR_AND_MASK macro [RAS], _rtmv2ref_rtm_ipv4_set_addr_and_mask, rras.rtm_ipv4_set_addr_and_mask, rtmv2/RTM_IPV4_SET_ADDR_AND_MASK
ms.topic: macro
req.header: rtmv2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Rtmv2.h
api_name:
 - RTM_IPV4_SET_ADDR_AND_MASK
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RTM_IPV4_SET_ADDR_AND_MASK macro


## -description


The 
<b>RTM_IPV4_SET_ADDR_AND_MASK</b> macro converts an IPv4 address and mask to a generic 
<a href="https://docs.microsoft.com/windows/desktop/api/rtmv2/ns-rtmv2-_rtm_net_address">RTM_NET_ADDRESS</a> structure.


## -parameters




### -param NetAddress

Receives the converted address structure.


### -param Addr

Specifies the IPv4 address to convert.


### -param Mask

Specifies the IPv4 mask to convert.


## -remarks



For example, if a client supplies the <i>Addr</i> 10.10.10.0 and the <i>Mask</i> 255.255.255.255, the <i>NetAddress</i> 10.10.10/24 is returned.

The macro is defined as follows:


```cpp
#include <windows.h>

#define RTM_IPV4_SET_ADDR_AND_MASK(NetAddress, Addr, Mask)  \
        (NetAddress)->AddressFamily = AF_INET;              \
        (* (ULONG *) ((NetAddress)->AddrBits)) = (Addr);    \
        RTM_IPV4_LEN_FROM_MASK((NetAddress)->NumBits, Mask)

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/rtmv2/nf-rtmv2-rtm_ipv4_get_addr_and_len">RTM_IPV4_GET_ADDR_AND_LEN</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rtmv2/nf-rtmv2-rtm_ipv4_get_addr_and_mask">RTM_IPV4_GET_ADDR_AND_MASK</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rtmv2/nf-rtmv2-rtm_ipv4_len_from_mask">RTM_IPV4_LEN_FROM_MASK</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rtmv2/nf-rtmv2-rtm_ipv4_make_net_address">RTM_IPV4_MAKE_NET_ADDRESS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rtmv2/nf-rtmv2-rtm_ipv4_mask_from_len">RTM_IPV4_MASK_FROM_LEN</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rtmv2/nf-rtmv2-rtm_ipv4_set_addr_and_len">RTM_IPV4_SET_ADDR_AND_LEN</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rtmv2/ns-rtmv2-_rtm_net_address">RTM_NET_ADDRESS</a>
 

 

