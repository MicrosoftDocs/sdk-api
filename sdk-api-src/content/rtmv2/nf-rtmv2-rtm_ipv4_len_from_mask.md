---
UID: NF:rtmv2.RTM_IPV4_LEN_FROM_MASK
title: RTM_IPV4_LEN_FROM_MASK macro (rtmv2.h)
description: The RTM_IPV4_LEN_FROM_MASK macro converts an IPv4 mask to a generic route length.
helpviewer_keywords: ["RTM_IPV4_LEN_FROM_MASK","RTM_IPV4_LEN_FROM_MASK macro [RAS]","_rtmv2ref_rtm_ipv4_len_from_mask","rras.rtm_ipv4_len_from_mask","rtmv2/RTM_IPV4_LEN_FROM_MASK"]
old-location: rras\rtm_ipv4_len_from_mask.htm
tech.root: RRAS
ms.assetid: fdbc2030-3917-4920-848e-76b5d1dfcfef
ms.date: 12/05/2018
ms.keywords: RTM_IPV4_LEN_FROM_MASK, RTM_IPV4_LEN_FROM_MASK macro [RAS], _rtmv2ref_rtm_ipv4_len_from_mask, rras.rtm_ipv4_len_from_mask, rtmv2/RTM_IPV4_LEN_FROM_MASK
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RTM_IPV4_LEN_FROM_MASK
 - rtmv2/RTM_IPV4_LEN_FROM_MASK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rtmv2.h
api_name:
 - RTM_IPV4_LEN_FROM_MASK
---

# RTM_IPV4_LEN_FROM_MASK macro


## -description

The 
<b>RTM_IPV4_LEN_FROM_MASK</b> macro converts an IPv4 mask to a generic route length.

## -parameters

### -param Len

Receives the converted length

### -param Mask

Specifies the mask to convert.

## -remarks

For example, if a client supplies the <i>Mask</i> 255.255.255.255, the <i>Len</i> 24 is returned.

The macro is defined as follows:


```cpp
#include <windows.h>

#define RTM_CHECK_NTH_BIT(Value, N, Len)                           \
        if ((Value) & (1 << (N)))                                  \
        {                                                          \
            (Len) += (N); (Value) <<= (N);                         \
        }

#define RTM_IPV4_LEN_FROM_MASK(Len, Mask)                   \
        {                                                   \
            ULONG _Temp_ = ntohl(Mask);                     \
            (Len) = 0;                                      \
            RTM_CHECK_NTH_BIT(_Temp_, 16, (Len));           \
            RTM_CHECK_NTH_BIT(_Temp_,  8, (Len));           \
            RTM_CHECK_NTH_BIT(_Temp_,  4, (Len));           \
            while (_Temp_)                                  \
            {                                               \
                (Len) +=  1; _Temp_ <<=  1;                 \
            }                                               \
        }                                                    \

```

## -see-also

<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtm_ipv4_get_addr_and_len">RTM_IPV4_GET_ADDR_AND_LEN</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtm_ipv4_get_addr_and_mask">RTM_IPV4_GET_ADDR_AND_MASK</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtm_ipv4_make_net_address">RTM_IPV4_MAKE_NET_ADDRESS</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtm_ipv4_mask_from_len">RTM_IPV4_MASK_FROM_LEN</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtm_ipv4_set_addr_and_len">RTM_IPV4_SET_ADDR_AND_LEN</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtm_ipv4_set_addr_and_mask">RTM_IPV4_SET_ADDR_AND_MASK</a>



<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_net_address">RTM_NET_ADDRESS</a>