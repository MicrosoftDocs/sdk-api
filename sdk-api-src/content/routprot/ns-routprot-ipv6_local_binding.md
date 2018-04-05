---
UID: NS:routprot.IPV6_LOCAL_BINDING
title: IPV6_LOCAL_BINDING
author: windows-driver-content
description: The IPV6_LOCAL_BINDING structure contains IPv6 address information for an adapter.
old-location: rras\ipv6_local_binding.htm
old-project: RRAS
ms.assetid: c698fa3b-04d5-4401-9ab3-a200211cff24
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PIPV6_LOCAL_BINDING, IPV6_LOCAL_BINDING, IPV6_LOCAL_BINDING structure [RAS], PIPV6_LOCAL_BINDING, PIPV6_LOCAL_BINDING structure pointer [RAS], routprot/IPV6_LOCAL_BINDING, routprot/PIPV6_LOCAL_BINDING, rras.ipv6_local_binding"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: IPV6_LOCAL_BINDING, *PIPV6_LOCAL_BINDING
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Routprot.h
api_name:
-	IPV6_LOCAL_BINDING
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPV6_LOCAL_BINDING structure


## -description


The 
<b>IPV6_LOCAL_BINDING</b> structure contains IPv6 address information for an adapter.


## -struct-fields




### -field Address

An <a href="https://msdn.microsoft.com/library/windows/hardware/ff554787">in6_addr</a> structure that specifies an IPv6 address for the adapter.


### -field PrefixLength

The length, in bits, of the address prefix.


## -remarks



Since an adapter can have more than one IP address, the 
<a href="https://msdn.microsoft.com/1e964f09-96c6-432b-bb1a-026a3ea0deba">IPV6_ADAPTER_BINDING_INFO</a> structure maintains an array of 
<b>IPV6_LOCAL_BINDING</b> structures.




## -see-also




<a href="https://msdn.microsoft.com/1e964f09-96c6-432b-bb1a-026a3ea0deba">IPV6_ADAPTER_BINDING_INFO</a>



<a href="https://msdn.microsoft.com/121cc415-35eb-4c9b-a02d-c23be468d6bc">IP_LOCAL_BINDING</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>



<a href="https://msdn.microsoft.com/767733eb-1cbd-4b8d-98b7-41d1d0f2c630">Router Management Structures</a>
 

 

