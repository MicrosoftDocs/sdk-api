---
UID: NS:clusapi._CLUSTER_IP_ENTRY
title: "_CLUSTER_IP_ENTRY"
author: windows-sdk-content
description: Describes an IP address for a cluster.
old-location: mscs\cluster_ip_entry.htm
old-project: mscs
ms.assetid: 9c2bc2ca-41e5-4e07-a3a2-d762ea5565e1
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: "*PCLUSTER_IP_ENTRY, CLUSTER_IP_ENTRY, CLUSTER_IP_ENTRY structure [Failover Cluster], PCLUSTER_IP_ENTRY, PCLUSTER_IP_ENTRY structure pointer [Failover Cluster], _CLUSTER_IP_ENTRY, clusapi/CLUSTER_IP_ENTRY, clusapi/PCLUSTER_IP_ENTRY, mscs.cluster_ip_entry"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: CLUSTER_IP_ENTRY, *PCLUSTER_IP_ENTRY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
api_name:
 - CLUSTER_IP_ENTRY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

