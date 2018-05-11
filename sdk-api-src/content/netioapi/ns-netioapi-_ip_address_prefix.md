---
UID: NS:netioapi._IP_ADDRESS_PREFIX
title: "_IP_ADDRESS_PREFIX"
author: windows-driver-content
description: Stores an IP address prefix.
old-location: iphlp\ip_address_prefix.htm
old-project: IpHlp
ms.assetid: 3a6598d8-77e4-46f7-9397-124157508207
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: "*PIP_ADDRESS_PREFIX, IP_ADDRESS_PREFIX, IP_ADDRESS_PREFIX structure [IP Helper], PIP_ADDRESS_PREFIX, PIP_ADDRESS_PREFIX structure pointer [IP Helper], _IP_ADDRESS_PREFIX, iphlp.ip_address_prefix, netioapi/IP_ADDRESS_PREFIX, netioapi/PIP_ADDRESS_PREFIX"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: netioapi.h
req.include-header: Iphlpapi.h
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
req.typenames: IP_ADDRESS_PREFIX, *PIP_ADDRESS_PREFIX
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Netioapi.h
api_name:
-	IP_ADDRESS_PREFIX
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# _IP_ADDRESS_PREFIX structure


## -description


The <b>IP_ADDRESS_PREFIX</b> structure  stores an IP address prefix.


## -struct-fields




### -field Prefix

The prefix or network part of IP the address represented as an IP address.

The <a href="https://msdn.microsoft.com/7278dcb4-65c6-4aea-a474-cb7fae4d7672">SOCKADDR_INET</a> union is defined in the <i>Ws2ipdef.h</i> header. 


### -field PrefixLength

The length, in bits, of the prefix or network part of the IP address. For a unicast IPv4 address, any value greater than 32 is an illegal value. For a unicast IPv6 address, any value greater than 128 is an illegal value. 
A value of 255 is commonly used to represent an illegal value. 


## -remarks



The <b>IP_ADDRESS_PREFIX</b> structure is defined on Windows Vista and later. 

The <b>IP_ADDRESS_PREFIX</b> structure is the data type of the <b>DestinationPrefix</b> member in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff559245">MIB_IPFORWARD_ROW2</a> structure.  A number of functions use the <b>MIB_IPFORWARD_ROW2</b> structure including <a href="https://msdn.microsoft.com/library/windows/hardware/ff546209">CreateIpForwardEntry2</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/ff546365">DeleteIpForwardEntry2</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/ff552511">GetBestRoute2</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/ff552535">GetIpForwardEntry2</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/ff552536">GetIpForwardTable2</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/ff554882">InitializeIpForwardEntry</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/ff568806">NotifyRouteChange2</a>, and <a href="https://msdn.microsoft.com/library/windows/hardware/ff570773">SetIpForwardEntry2</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff546209">CreateIpForwardEntry2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546365">DeleteIpForwardEntry2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552511">GetBestRoute2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552535">GetIpForwardEntry2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552536">GetIpForwardTable2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff554882">InitializeIpForwardEntry</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff559245">MIB_IPFORWARD_ROW2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff568806">NotifyRouteChange2</a>



<a href="https://msdn.microsoft.com/7278dcb4-65c6-4aea-a474-cb7fae4d7672">SOCKADDR_INET</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570773">SetIpForwardEntry2</a>
 

 

