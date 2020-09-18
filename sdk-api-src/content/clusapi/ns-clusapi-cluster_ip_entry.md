---
UID: NS:clusapi._CLUSTER_IP_ENTRY
title: CLUSTER_IP_ENTRY (clusapi.h)
description: Describes an IP address for a cluster.
helpviewer_keywords: ["*PCLUSTER_IP_ENTRY","CLUSTER_IP_ENTRY","CLUSTER_IP_ENTRY structure [Failover Cluster]","PCLUSTER_IP_ENTRY","PCLUSTER_IP_ENTRY structure pointer [Failover Cluster]","clusapi/CLUSTER_IP_ENTRY","clusapi/PCLUSTER_IP_ENTRY","mscs.cluster_ip_entry"]
old-location: mscs\cluster_ip_entry.htm
tech.root: MsCS
ms.assetid: 9c2bc2ca-41e5-4e07-a3a2-d762ea5565e1
ms.date: 12/05/2018
ms.keywords: '*PCLUSTER_IP_ENTRY, CLUSTER_IP_ENTRY, CLUSTER_IP_ENTRY structure [Failover Cluster], PCLUSTER_IP_ENTRY, PCLUSTER_IP_ENTRY structure pointer [Failover Cluster], clusapi/CLUSTER_IP_ENTRY, clusapi/PCLUSTER_IP_ENTRY, mscs.cluster_ip_entry'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CLUSTER_IP_ENTRY, *PCLUSTER_IP_ENTRY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CLUSTER_IP_ENTRY
 - clusapi/_CLUSTER_IP_ENTRY
 - PCLUSTER_IP_ENTRY
 - clusapi/PCLUSTER_IP_ENTRY
 - CLUSTER_IP_ENTRY
 - clusapi/CLUSTER_IP_ENTRY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
api_name:
 - CLUSTER_IP_ENTRY
---

# CLUSTER_IP_ENTRY structure


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
    <a href="/windows/desktop/api/clusapi/ns-clusapi-create_cluster_config">CREATE_CLUSTER_CONFIG</a> structure, which is in turn 
    passed as the <i>pConfig</i> parameter of the 
    <a href="/windows/desktop/api/clusapi/nf-clusapi-createcluster">CreateCluster</a> function.

## -see-also

<a href="/windows/desktop/api/clusapi/ns-clusapi-create_cluster_config">CREATE_CLUSTER_CONFIG</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-createcluster">CreateCluster</a>



<a href="/previous-versions/windows/desktop/mscs/utility-structures">Utility structures</a>