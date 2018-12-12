---
UID: NS:ipexport._IPV6_ADDRESS_EX
title: IPV6_ADDRESS_EX
author: windows-sdk-content
description: Stores an IPv6 address.
old-location: iphlp\ipv6_address_ex.htm
tech.root: IpHlp
ms.assetid: 68c9e941-bbc4-4506-949d-efd16c15d5b9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PIPV6_ADDRESS_EX, IPV6_ADDRESS_EX, IPV6_ADDRESS_EX structure [IP Helper], PIPV6_ADDRESS_EX, PIPV6_ADDRESS_EX structure pointer [IP Helper], ipexport/IPV6_ADDRESS_EX, ipexport/PIPV6_ADDRESS_EX, iphlp.ipv6_address_ex"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ipexport.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - Ipexport.h
api_name:
 - IPV6_ADDRESS_EX
product: Windows
targetos: Windows
req.typenames: IPV6_ADDRESS_EX, *PIPV6_ADDRESS_EX
req.redist: 
---

# IPV6_ADDRESS_EX structure


## -description


The <b>IPV6_ADDRESS_EX</b> structure stores an 
    IPv6 address.


## -struct-fields




### -field sin6_port

The IPv6 port number in network byte order.


### -field sin6_flowinfo

The IPv6 flowinfo value from the IPv6 header in network byte order.


### -field sin6_addr

The IPv6 address in network byte order.


### -field sin6_scope_id

The IPv6 scope ID in network byte order.


## -remarks



The <b>IPV6_ADDRESS_EX</b> structure is a member of the 
     <a href="https://msdn.microsoft.com/8ea4ce42-6164-4b8e-9e79-524f456c8d09">ICMPV6_ECHO_REPLY</a> structure that is used by the 
     <a href="https://msdn.microsoft.com/b4d63ffd-37ad-4901-b017-205fb15381e7">Icmp6ParseReplies</a> function. 

The <b>IPV6_ADDRESS_EX</b> structure is defined in public 
     header files included in the Microsoft Windows Software Development Kit (SDK), but this structure is used by the 
     <a href="https://msdn.microsoft.com/b4d63ffd-37ad-4901-b017-205fb15381e7">Icmp6ParseReplies</a> function on 
     Windows XP and later. 

In the Windows SDK, the 
     <b>IPV6_ADDRESS_EX</b> is structure defined when compiling an 
     application if the target platform is Windows XP and later 
     (<code>NTDDI_VERSION &gt;= NTDDI_XP</code>, 
     <code>_WIN32_WINNT &gt;= 0x0501</code>, or 
     <code>WINVER &gt;= 0x0501</code>). When compiling an application if the target 
     platform is not Windows XP and later, the 
     <b>IPV6_ADDRESS_EX</b> structure is undefined.

This structure is defined in the Ipexport.h header file which is automatically included in the Iphlpapi.h 
     header file. The Ipexport.h header file should never be used directly.




## -see-also




<a href="https://msdn.microsoft.com/8ea4ce42-6164-4b8e-9e79-524f456c8d09">ICMPV6_ECHO_REPLY</a>



<a href="https://msdn.microsoft.com/4896a9f8-0486-4380-bf49-d1c9ef114acc">IP Helper Start Page</a>



<a href="https://msdn.microsoft.com/d53c3821-00a0-4eaa-9a06-69ec7aa98d84">IP Helper Structures</a>



<a href="https://msdn.microsoft.com/4341d0a4-65d8-4677-b208-2cde5ff36f14">IP_OPTION_INFORMATION</a>



<a href="https://msdn.microsoft.com/2ddb23d8-a4e6-47c4-a552-2815ccaf055f">Icmp6CreateFile</a>



<a href="https://msdn.microsoft.com/b4d63ffd-37ad-4901-b017-205fb15381e7">Icmp6ParseReplies</a>



<a href="https://msdn.microsoft.com/622c769b-ede8-4bc2-ac54-98de47ae1fed">Icmp6SendEcho2</a>



<a href="https://msdn.microsoft.com/ce8f11bb-1e33-41bd-adb9-c18efadd4d0b">IcmpCloseHandle</a>
 

 

