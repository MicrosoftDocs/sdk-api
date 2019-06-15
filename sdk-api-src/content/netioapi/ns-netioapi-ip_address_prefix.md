---
UID: NS:netioapi._IP_ADDRESS_PREFIX
title: IP_ADDRESS_PREFIX (netioapi.h)
author: windows-sdk-content
description: Stores an IP address prefix.
old-location: iphlp\ip_address_prefix.htm
tech.root: IpHlp
ms.assetid: 3a6598d8-77e4-46f7-9397-124157508207
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PIP_ADDRESS_PREFIX, IP_ADDRESS_PREFIX, IP_ADDRESS_PREFIX structure [IP Helper], PIP_ADDRESS_PREFIX, PIP_ADDRESS_PREFIX structure pointer [IP Helper], _IP_ADDRESS_PREFIX, iphlp.ip_address_prefix, netioapi/IP_ADDRESS_PREFIX, netioapi/PIP_ADDRESS_PREFIX"
ms.topic: struct
f1_keywords: ["netioapi/IP_ADDRESS_PREFIX"]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Netioapi.h
api_name:
 - IP_ADDRESS_PREFIX
product: Windows
targetos: Windows
req.typenames: IP_ADDRESS_PREFIX, *PIP_ADDRESS_PREFIX
req.redist: 
ms.custom: 19H1
---

# IP_ADDRESS_PREFIX structure


## -description


The <b>IP_ADDRESS_PREFIX</b> structure  stores an IP address prefix.


## -struct-fields




### -field Prefix

The prefix or network part of IP the address represented as an IP address.

The <a href="https://docs.microsoft.com/windows/desktop/api/ws2ipdef/ns-ws2ipdef-_sockaddr_inet">SOCKADDR_INET</a> union is defined in the <i>Ws2ipdef.h</i> header. 


### -field PrefixLength

The length, in bits, of the prefix or network part of the IP address. For a unicast IPv4 address, any value greater than 32 is an illegal value. For a unicast IPv6 address, any value greater than 128 is an illegal value. 
A value of 255 is commonly used to represent an illegal value. 


## -remarks



The <b>IP_ADDRESS_PREFIX</b> structure is defined on Windows Vista and later. 

The <b>IP_ADDRESS_PREFIX</b> structure is the data type of the <b>DestinationPrefix</b> member in the <a href="https://docs.microsoft.com/windows/desktop/api/netioapi/ns-netioapi-_mib_ipforward_row2">MIB_IPFORWARD_ROW2</a> structure.  A number of functions use the <b>MIB_IPFORWARD_ROW2</b> structure including <a href="https://docs.microsoft.com/windows/desktop/api/netioapi/nf-netioapi-createipforwardentry2">CreateIpForwardEntry2</a>, <a href="https://docs.microsoft.com/windows/desktop/api/netioapi/nf-netioapi-deleteipforwardentry2">DeleteIpForwardEntry2</a>, <a href="https://docs.microsoft.com/windows/desktop/api/netioapi/nf-netioapi-getbestroute2">GetBestRoute2</a>, <a href="https://docs.microsoft.com/windows/desktop/api/netioapi/nf-netioapi-getipforwardentry2">GetIpForwardEntry2</a>, <a href="https://docs.microsoft.com/windows/desktop/api/netioapi/nf-netioapi-getipforwardtable2">GetIpForwardTable2</a>, <a href="https://docs.microsoft.com/windows/desktop/api/netioapi/nf-netioapi-initializeipforwardentry">InitializeIpForwardEntry</a>, <a href="https://docs.microsoft.com/windows/desktop/api/netioapi/nf-netioapi-notifyroutechange2">NotifyRouteChange2</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/netioapi/nf-netioapi-setipforwardentry2">SetIpForwardEntry2</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/netioapi/nf-netioapi-createipforwardentry2">CreateIpForwardEntry2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/netioapi/nf-netioapi-deleteipforwardentry2">DeleteIpForwardEntry2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/netioapi/nf-netioapi-getbestroute2">GetBestRoute2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/netioapi/nf-netioapi-getipforwardentry2">GetIpForwardEntry2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/netioapi/nf-netioapi-getipforwardtable2">GetIpForwardTable2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/netioapi/nf-netioapi-initializeipforwardentry">InitializeIpForwardEntry</a>



<a href="https://docs.microsoft.com/windows/desktop/api/netioapi/ns-netioapi-_mib_ipforward_row2">MIB_IPFORWARD_ROW2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/netioapi/nf-netioapi-notifyroutechange2">NotifyRouteChange2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2ipdef/ns-ws2ipdef-_sockaddr_inet">SOCKADDR_INET</a>



<a href="https://docs.microsoft.com/windows/desktop/api/netioapi/nf-netioapi-setipforwardentry2">SetIpForwardEntry2</a>
 

 

