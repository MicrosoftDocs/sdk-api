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

# _DHCP_CLIENT_SEARCH_INFO_V6 structure


## -description


The <b>DHCP_SEARCH_INFO_V6</b> structure contains the term or value on which the DHCPv6 server database will be searched.


## -struct-fields




### -field SearchType

Enumeration value that selects the type of the value on which the DHCPv6 database will be searched.



##### )



#####  )



##### )


### -field SearchInfo.ClientIpAddress.case

 


### -field SearchInfo.ClientIpAddress.case.Dhcpv6ClientIpAddress

 


### -field SearchInfo.ClientDUID.case

 


### -field SearchInfo.ClientDUID.case.Dhcpv6ClientDUID

 


### -field SearchInfo.ClientName.case

 


### -field SearchInfo.ClientName.case.Dhcpv6ClientName

 


### -field SearchInfo.switch_is

 


### -field SearchInfo.switch_is.SearchType

 


### -field SearchInfo.switch_type

 


### -field SearchInfo.switch_type.DHCP_SEARCH_INFO_TYPE_V6

 


### -field SearchInfo


### -field SearchInfo.ClientIpAddress


<a href="https://msdn.microsoft.com/9623e866-81e5-4d5a-8801-33f0f8973ed3">DHCP_IPV6_ADDRESS</a> structure that specifies the client IPv6 address to search for.


### -field SearchInfo.ClientDUID

GUID value that specifies the client DHCP UID to search for.


### -field SearchInfo.ClientName

Unicode string that specifies the client name to search for.


### -field _DHCP_CLIENT_SEARCH_UNION_V6

 




## -see-also




<a href="https://msdn.microsoft.com/56c2cbda-4af5-4f28-9b1f-be7d6cf0c1f5">DHCP_SEARCH_INFO_TYPE_V6</a>
 

 

