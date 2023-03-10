---
UID: NS:clusapi.CLUS_NETNAME_IP_INFO_ENTRY
title: CLUS_NETNAME_IP_INFO_ENTRY (clusapi.h)
description: Represents IP information for a NetName resource.
helpviewer_keywords: ["*PCLUS_NETNAME_IP_INFO_ENTRY","CLUS_NETNAME_IP_INFO_ENTRY","CLUS_NETNAME_IP_INFO_ENTRY structure [Failover Cluster]","PCLUS_NETNAME_IP_INFO_ENTRY","PCLUS_NETNAME_IP_INFO_ENTRY structure pointer [Failover Cluster]","clusapi/CLUS_NETNAME_IP_INFO_ENTRY","clusapi/PCLUS_NETNAME_IP_INFO_ENTRY","mscs.clus_netname_ip_info_entry"]
old-location: mscs\clus_netname_ip_info_entry.htm
tech.root: MsCS
ms.assetid: 9631BDB9-6B7C-4BFF-9654-20C77F851A22
ms.date: 12/05/2018
ms.keywords: '*PCLUS_NETNAME_IP_INFO_ENTRY, CLUS_NETNAME_IP_INFO_ENTRY, CLUS_NETNAME_IP_INFO_ENTRY structure [Failover Cluster], PCLUS_NETNAME_IP_INFO_ENTRY, PCLUS_NETNAME_IP_INFO_ENTRY structure pointer [Failover Cluster], clusapi/CLUS_NETNAME_IP_INFO_ENTRY, clusapi/PCLUS_NETNAME_IP_INFO_ENTRY, mscs.clus_netname_ip_info_entry'
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2 Datacenter, Windows Server 2008 R2 Enterprise
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
req.typenames: CLUS_NETNAME_IP_INFO_ENTRY, *PCLUS_NETNAME_IP_INFO_ENTRY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUS_NETNAME_IP_INFO_ENTRY
 - clusapi/CLUS_NETNAME_IP_INFO_ENTRY
 - PCLUS_NETNAME_IP_INFO_ENTRY
 - clusapi/PCLUS_NETNAME_IP_INFO_ENTRY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusApi.h
api_name:
 - CLUS_NETNAME_IP_INFO_ENTRY
---

# CLUS_NETNAME_IP_INFO_ENTRY structure


## -description

Represents IP information for a NetName resource.

## -struct-fields

### -field NodeId

The ID of the node that hosts the NetName resource.

### -field AddressSize

The size of the <i>BYTE</i> parameter, in bytes.

### -field Address

A byte array that contains the address of the NetName.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/utility-structures">Utility structures</a>