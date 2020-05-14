---
UID: NF:rtmv2.RTM_IPV4_MASK_FROM_LEN
title: RTM_IPV4_MASK_FROM_LEN macro (rtmv2.h)
description: The RTM_IPV4_MASK_FROM_LEN macro converts a generic route length to an IPv4 mask.helpviewer_keywords: ["RTM_IPV4_MASK_FROM_LEN","RTM_IPV4_MASK_FROM_LEN macro [RAS]","_rtmv2ref_rtm_ipv4_mask_from_len","rras.rtm_ipv4_mask_from_len","rtmv2/RTM_IPV4_MASK_FROM_LEN"]
old-location: rras\rtm_ipv4_mask_from_len.htm
tech.root: RRAS
ms.assetid: 7f4a67d9-e707-413e-8cc3-600eb7968b82
ms.date: 12/05/2018
ms.keywords: RTM_IPV4_MASK_FROM_LEN, RTM_IPV4_MASK_FROM_LEN macro [RAS], _rtmv2ref_rtm_ipv4_mask_from_len, rras.rtm_ipv4_mask_from_len, rtmv2/RTM_IPV4_MASK_FROM_LEN
f1_keywords:
- rtmv2/RTM_IPV4_MASK_FROM_LEN
dev_langs:
- c++
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
- RTM_IPV4_MASK_FROM_LEN
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RTM_IPV4_MASK_FROM_LEN macro


## -description


The 
<b>RTM_IPV4_MASK_FROM_LEN</b> macro converts a generic route length to an IPv4 mask.


## -parameters




### -param Len

Specifies the generic length to convert.


## -remarks



For example, if a client supplies the <i>Len</i> 24, the mask 255.255.255.255 is returned.

The macro is defined as follows:


```cpp
#include <windows.h>

#define RTM_IPV4_MASK_FROM_LEN(Len)                         \
        ((Len) ? htonl(~0 << (32 - (Len))): 0);             \       

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/rtmv2/nf-rtmv2-rtm_ipv4_get_addr_and_len">RTM_IPV4_GET_ADDR_AND_LEN</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rtmv2/nf-rtmv2-rtm_ipv4_get_addr_and_mask">RTM_IPV4_GET_ADDR_AND_MASK</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rtmv2/nf-rtmv2-rtm_ipv4_len_from_mask">RTM_IPV4_LEN_FROM_MASK</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rtmv2/nf-rtmv2-rtm_ipv4_make_net_address">RTM_IPV4_MAKE_NET_ADDRESS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rtmv2/nf-rtmv2-rtm_ipv4_set_addr_and_len">RTM_IPV4_SET_ADDR_AND_LEN</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rtmv2/nf-rtmv2-rtm_ipv4_set_addr_and_mask">RTM_IPV4_SET_ADDR_AND_MASK</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rtmv2/ns-rtmv2-rtm_net_address">RTM_NET_ADDRESS</a>
 

 

