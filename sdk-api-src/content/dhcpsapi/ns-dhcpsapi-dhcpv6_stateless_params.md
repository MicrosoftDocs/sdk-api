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

# DHCPV6_STATELESS_PARAMS structure


## -description


The <b>DHCPV6_STATELESS_PARAMS</b> structure defines the DHCPv6 stateless client inventory configuration settings at server and scope level.


## -struct-fields




### -field Status

If <b>TRUE</b> the stateless client inventory is maintained by the DHCPv6 server. Otherwise, it is  <b>FALSE</b>. The default value is <b>FALSE</b>, which indicates that the stateless client inventory is disabled and is not maintained the by the server.


### -field PurgeInterval

Integer that specifies the maximum time interval, in hours, that stateless IPv6 DHCP client lease records can persist before being deleted from the DHCP server database.


## -see-also




<a href="https://msdn.microsoft.com/8670c69b-1fc0-4b60-b5cc-a616d56c9319">DHCPV6_STATELESS_PARAM_TYPE</a>



<a href="https://msdn.microsoft.com/80a32132-a032-452f-9438-52a1eb280fdf">Dhcpv6GetStatelessStoreParams</a>



<a href="https://msdn.microsoft.com/8f64c1bb-8f02-45e3-b9ed-8fce2bf9885c">Dhcpv6SetStatelessStoreParams</a>
 

 

