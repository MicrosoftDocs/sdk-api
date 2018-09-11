---
UID: NS:iptypes._IP_PER_ADAPTER_INFO_W2KSP1
title: "_IP_PER_ADAPTER_INFO_W2KSP1"
author: windows-sdk-content
description: The IP_PER_ADAPTER_INFO structure contains information specific to a particular adapter.
old-location: iphlp\ip_per_adapter_info.htm
tech.root: iphlp
ms.assetid: 10cfdded-4184-4d34-9ccd-85446c13d497
ms.author: windowssdkdev
ms.date: 08/15/2018
ms.keywords: "*PIP_PER_ADAPTER_INFO, *PIP_PER_ADAPTER_INFO_W2KSP1, IP_PER_ADAPTER_INFO, IP_PER_ADAPTER_INFO structure [IP Helper], IP_PER_ADAPTER_INFO_W2KSP1, PIP_PER_ADAPTER_INFO, PIP_PER_ADAPTER_INFO structure pointer [IP Helper], _IP_PER_ADAPTER_INFO_W2KSP1, _iphlp_ip_per_adapter_info, iphlp.ip_per_adapter_info, iptypes/IP_PER_ADAPTER_INFO, iptypes/PIP_PER_ADAPTER_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: iptypes.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
 - Iptypes.h
api_name:
 - IP_PER_ADAPTER_INFO
product: Windows
targetos: Windows
req.typenames: IP_PER_ADAPTER_INFO_W2KSP1, *PIP_PER_ADAPTER_INFO_W2KSP1
req.redist: 
---

# _IP_PER_ADAPTER_INFO_W2KSP1 structure


## -description


The 
<b>IP_PER_ADAPTER_INFO</b> structure contains information specific to a particular adapter.


## -struct-fields




### -field AutoconfigEnabled

Specifies whether IP address auto-configuration (APIPA) is enabled on this adapter. See Remarks. 


### -field AutoconfigActive

Specifies whether this adapter's IP address is currently auto-configured by APIPA.


### -field CurrentDnsServer

Reserved. Use the <b>DnsServerList</b> member to obtain the DNS servers for the local computer.


### -field DnsServerList

A linked list of 
<a href="https://msdn.microsoft.com/783c383d-7fd3-45bc-90f6-2e8ce01db3c3">IP_ADDR_STRING</a> structures that specify the set of DNS servers used by the local computer.


## -remarks



APIPA enables automatic IP address configuration on networks without DHCP servers, using the IANA-reserved Class B network 169.254.0.0, with a subnet mask of 255.255.0.0. Clients send ARP messages to ensure the selected address is not currently in use. Clients auto-configured in this fashion continue to poll for a valid DHCP server every five minutes, and if found, the DHCP server configuration overrides all auto-configuration settings.




## -see-also




<a href="https://msdn.microsoft.com/fc1ae7e4-f856-4b48-8ab4-56cd511ed161">GetPerAdapterInfo</a>



<a href="https://msdn.microsoft.com/4896a9f8-0486-4380-bf49-d1c9ef114acc">IP Helper Start Page</a>



<a href="https://msdn.microsoft.com/d53c3821-00a0-4eaa-9a06-69ec7aa98d84">IP Helper Structures</a>



<a href="https://msdn.microsoft.com/783c383d-7fd3-45bc-90f6-2e8ce01db3c3">IP_ADDR_STRING</a>
 

 

