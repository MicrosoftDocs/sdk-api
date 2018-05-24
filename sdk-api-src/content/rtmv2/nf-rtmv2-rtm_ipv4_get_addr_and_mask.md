---
UID: NF:rtmv2.RTM_IPV4_GET_ADDR_AND_MASK
title: RTM_IPV4_GET_ADDR_AND_MASK macro
author: windows-driver-content
description: The RTM_IPV4_GET_ADDR_AND_MASK macro converts to a generic RTM_NET_ADDRESS structure and length to an IPv4 address and mask.
old-location: rras\rtm_ipv4_get_addr_and_mask.htm
old-project: RRAS
ms.assetid: 2dd2c01b-41f1-48e3-942b-954f7b2efac5
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: RTM_IPV4_GET_ADDR_AND_MASK, RTM_IPV4_GET_ADDR_AND_MASK macro [RAS], _rtmv2ref_rtm_ipv4_get_addr_and_mask, rras.rtm_ipv4_get_addr_and_mask, rtmv2/RTM_IPV4_GET_ADDR_AND_MASK
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: RTM_EVENT_TYPE, *PRTM_EVENT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Rtmv2.h
api_name:
-	RTM_IPV4_GET_ADDR_AND_MASK
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# RTM_IPV4_GET_ADDR_AND_MASK macro


## -description


The 
<b>RTM_IPV4_GET_ADDR_AND_MASK</b> macro converts to a generic 
<a href="https://msdn.microsoft.com/92c4e797-9b73-438d-b4df-9739fae9d5c8">RTM_NET_ADDRESS</a> structure and length to an IPv4 address and mask.


## -parameters




### -param Addr

Receives the converted IPv4 address.


### -param Mask

Receives the converted IPv4 mask.


### -param NetAddress

Specifies the network address to convert.


## -remarks



For example, if a client supplies the <i>NetAddress</i> 10.10.10.24, the <i>Addr</i> 10.10.10.0 and the <i>Mask</i> 255.255.255.255 are returned.

The macro is defined as follows:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;

#define RTM_IPV4_GET_ADDR_AND_MASK(Addr, Mask, NetAddress)  \
        (Addr) = (* (ULONG *) ((NetAddress)-&gt;AddrBits));    \
        (Mask) = RTM_IPV4_MASK_FROM_LEN((NetAddress)-       \
            &gt;NumBits);   
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/e37bb309-845c-4685-bbfd-15ffc6c74fd0">RTM_IPV4_GET_ADDR_AND_LEN</a>



<a href="https://msdn.microsoft.com/fdbc2030-3917-4920-848e-76b5d1dfcfef">RTM_IPV4_LEN_FROM_MASK</a>



<a href="https://msdn.microsoft.com/9a5d9ee0-8199-420b-9489-068d1171e647">RTM_IPV4_MAKE_NET_ADDRESS</a>



<a href="https://msdn.microsoft.com/7f4a67d9-e707-413e-8cc3-600eb7968b82">RTM_IPV4_MASK_FROM_LEN</a>



<a href="https://msdn.microsoft.com/c6f60346-51ff-4e1e-9edb-b326184f79cf">RTM_IPV4_SET_ADDR_AND_LEN</a>



<a href="https://msdn.microsoft.com/23849eed-309a-41b8-b853-1267806166fa">RTM_IPV4_SET_ADDR_AND_MASK</a>



<a href="https://msdn.microsoft.com/92c4e797-9b73-438d-b4df-9739fae9d5c8">RTM_NET_ADDRESS</a>
 

 

