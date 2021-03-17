---
UID: NF:rtmv2.RTM_IPV4_MAKE_NET_ADDRESS
title: RTM_IPV4_MAKE_NET_ADDRESS macro (rtmv2.h)
description: The RTM_IPV4_MAKE_NET_ADDRESS macro converts an IPv4 address and a length to a generic RTM_NET_ADDRESS structure.
helpviewer_keywords: ["RTM_IPV4_MAKE_NET_ADDRESS","RTM_IPV4_MAKE_NET_ADDRESS macro [RAS]","_rtmv2ref_rtm_ipv4_make_net_address","rras.rtm_ipv4_make_net_address","rtmv2/RTM_IPV4_MAKE_NET_ADDRESS"]
old-location: rras\rtm_ipv4_make_net_address.htm
tech.root: RRAS
ms.assetid: 9a5d9ee0-8199-420b-9489-068d1171e647
ms.date: 12/05/2018
ms.keywords: RTM_IPV4_MAKE_NET_ADDRESS, RTM_IPV4_MAKE_NET_ADDRESS macro [RAS], _rtmv2ref_rtm_ipv4_make_net_address, rras.rtm_ipv4_make_net_address, rtmv2/RTM_IPV4_MAKE_NET_ADDRESS
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
 - RTM_IPV4_MAKE_NET_ADDRESS
 - rtmv2/RTM_IPV4_MAKE_NET_ADDRESS
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
 - RTM_IPV4_MAKE_NET_ADDRESS
---

# RTM_IPV4_MAKE_NET_ADDRESS macro


## -description

The 
<b>RTM_IPV4_MAKE_NET_ADDRESS</b> macro converts an IPv4 address and a length to a generic 
<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_net_address">RTM_NET_ADDRESS</a> structure.

## -parameters

### -param NetAddress

Receives the converted address structure.

### -param Addr

Specifies the IPv4 address to convert.

### -param Len

Specifies the length to convert.

## -remarks

For example, if a client supplies the <i>Addr</i> 10.10.10.0 and the <i>Len</i> 24, the <i>NetAddress</i> 10.10.10/24 is returned.

The macro is defined as follows:


```cpp
#include <windows.h>

#define RTM_IPV4_MAKE_NET_ADDRESS(NetAddress, Addr, Len)    \
        RTM_IPV4_SET_ADDR_AND_LEN(NetAddress, Addr, Len)      

```

## -see-also

<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtm_ipv4_get_addr_and_len">RTM_IPV4_GET_ADDR_AND_LEN</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtm_ipv4_get_addr_and_mask">RTM_IPV4_GET_ADDR_AND_MASK</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtm_ipv4_len_from_mask">RTM_IPV4_LEN_FROM_MASK</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtm_ipv4_mask_from_len">RTM_IPV4_MASK_FROM_LEN</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtm_ipv4_set_addr_and_len">RTM_IPV4_SET_ADDR_AND_LEN</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtm_ipv4_set_addr_and_mask">RTM_IPV4_SET_ADDR_AND_MASK</a>



<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_net_address">RTM_NET_ADDRESS</a>