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

# _CLUSTER_IP_ENTRY structure


## -description


Describes an IP address for a cluster.


## -struct-fields




### -field lpszIpAddress

A <b>NULL</b>-terminated Unicode string containing a valid IPv4 or IPv6 numeric network 
      address.


### -field dwPrefixLength

Specifies the number of bits in the subnet mask, for example 24 for an IPv4 netmask of 255.255.255.0.


## -remarks



To specify a DHCP address, use the network identifier (all bits in the subnet set to 0) and the subnet prefix 
    length. For example, if the DHCP server hands out addresses in the 192.168.1.0/24 address block (from 192.168.1.0 
    through 192.168.1.255), specify "192.168.1.0" for the <b>lpszIpAddress</b> 
    member and 24 for the <b>dwPrefixLength</b> member.

A pointer to an array of <b>CLUSTER_IP_ENTRY</b> 
    structures is passed in the <b>pIpEntries</b> member of the 
    <a href="https://msdn.microsoft.com/5fc90422-47e4-44da-a49f-66d4b7712f53">CREATE_CLUSTER_CONFIG</a> structure, which is in turn 
    passed as the <i>pConfig</i> parameter of the 
    <a href="https://msdn.microsoft.com/672a1573-63e5-4321-a049-25bdafc1b5e0">CreateCluster</a> function.




## -see-also




<a href="https://msdn.microsoft.com/5fc90422-47e4-44da-a49f-66d4b7712f53">CREATE_CLUSTER_CONFIG</a>



<a href="https://msdn.microsoft.com/672a1573-63e5-4321-a049-25bdafc1b5e0">CreateCluster</a>



<a href="https://msdn.microsoft.com/45da8dbc-dd70-4f95-b933-66d8e4340448">Utility structures</a>
 

 

