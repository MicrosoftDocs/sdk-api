---
UID: NS:routprot.IPV6_ADAPTER_BINDING_INFO
title: IPV6_ADAPTER_BINDING_INFO (routprot.h)
author: windows-sdk-content
description: The IPV6_ADAPTER_BINDING_INFO structure contains IPv6-specific information for a particular network adapter.
old-location: rras\ipv6_adapter_binding_info.htm
tech.root: RRAS
ms.assetid: 1e964f09-96c6-432b-bb1a-026a3ea0deba
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PIPV6_ADAPTER_BINDING_INFO, IPV6_ADAPTER_BINDING_INFO, IPV6_ADAPTER_BINDING_INFO structure [RAS], PIPV6_ADAPTER_BINDING_INFO, PIPV6_ADAPTER_BINDING_INFO structure pointer [RAS], routprot/IPV6_ADAPTER_BINDING_INFO, routprot/PIPV6_ADAPTER_BINDING_INFO, rras.ipv6_adapter_binding_info"
ms.topic: struct
req.header: routprot.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - Routprot.h
api_name:
 - IPV6_ADAPTER_BINDING_INFO
product: Windows
targetos: Windows
req.typenames: IPV6_ADAPTER_BINDING_INFO, *PIPV6_ADAPTER_BINDING_INFO
req.redist: 
---

# IPV6_ADAPTER_BINDING_INFO structure


## -description


The 
<b>IPV6_ADAPTER_BINDING_INFO</b> structure contains IPv6-specific information for a particular network adapter.


## -struct-fields




### -field AddressCount

The number of IPv6 addresses associated with this adapter.


### -field RemoteAddress

This member is for WAN interfaces. An <a href="https://msdn.microsoft.com/2029db76-3fe1-4560-b753-910c48cbc578">in6_addr</a> structure that contains the address of the machine at the other end of a dial-up link.


### -field Mtu

Reserved for future use.


### -field Speed

Reserved for future use.


### -field Address

Pointer to an array of 
<a href="https://msdn.microsoft.com/c698fa3b-04d5-4401-9ab3-a200211cff24">IPV6_LOCAL_BINDING</a> structures. The array  contains a structure for each of the IPv6 addresses associated with this adapter.


## -remarks



Since an adapter can have more than one IP address, the 
<b>IPV6_ADAPTER_BINDING_INFO</b> structure maintains an array of 
<a href="https://msdn.microsoft.com/c698fa3b-04d5-4401-9ab3-a200211cff24">IPV6_LOCAL_BINDING</a> structures.




## -see-also




<a href="https://msdn.microsoft.com/c698fa3b-04d5-4401-9ab3-a200211cff24">IPV6_LOCAL_BINDING</a>



<a href="https://msdn.microsoft.com/3eb864e7-2de6-44c2-af3e-fee547de6081">IP_ADAPTER_BINDING_INFO</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>



<a href="https://msdn.microsoft.com/767733eb-1cbd-4b8d-98b7-41d1d0f2c630">Router Management Structures</a>
 

 

