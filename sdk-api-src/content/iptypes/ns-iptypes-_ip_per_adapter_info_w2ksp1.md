---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

