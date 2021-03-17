---
UID: NS:clusapi.CLUS_NETNAME_IP_INFO_FOR_MULTICHANNEL
title: CLUS_NETNAME_IP_INFO_FOR_MULTICHANNEL (clusapi.h)
description: Represents IP information for a NetName resource that has Multichannel enabled.
helpviewer_keywords: ["*PCLUS_NETNAME_IP_INFO_FOR_MULTICHANNEL","CLUS_NETNAME_IP_INFO_FOR_MULTICHANNEL","CLUS_NETNAME_IP_INFO_FOR_MULTICHANNEL structure [Failover Cluster]","PCLUS_NETNAME_IP_INFO_FOR_MULTICHANNEL","PCLUS_NETNAME_IP_INFO_FOR_MULTICHANNEL structure pointer [Failover Cluster]","clusapi/CLUS_NETNAME_IP_INFO_FOR_MULTICHANNEL","clusapi/PCLUS_NETNAME_IP_INFO_FOR_MULTICHANNEL","mscs.clus_netname_ip_info_for_multichannel"]
old-location: mscs\clus_netname_ip_info_for_multichannel.htm
tech.root: MsCS
ms.assetid: 724FD774-00F4-4617-B761-87509AD61AF4
ms.date: 12/05/2018
ms.keywords: '*PCLUS_NETNAME_IP_INFO_FOR_MULTICHANNEL, CLUS_NETNAME_IP_INFO_FOR_MULTICHANNEL, CLUS_NETNAME_IP_INFO_FOR_MULTICHANNEL structure [Failover Cluster], PCLUS_NETNAME_IP_INFO_FOR_MULTICHANNEL, PCLUS_NETNAME_IP_INFO_FOR_MULTICHANNEL structure pointer [Failover Cluster], clusapi/CLUS_NETNAME_IP_INFO_FOR_MULTICHANNEL, clusapi/PCLUS_NETNAME_IP_INFO_FOR_MULTICHANNEL, mscs.clus_netname_ip_info_for_multichannel'
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
req.typenames: CLUS_NETNAME_IP_INFO_FOR_MULTICHANNEL, *PCLUS_NETNAME_IP_INFO_FOR_MULTICHANNEL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUS_NETNAME_IP_INFO_FOR_MULTICHANNEL
 - clusapi/CLUS_NETNAME_IP_INFO_FOR_MULTICHANNEL
 - PCLUS_NETNAME_IP_INFO_FOR_MULTICHANNEL
 - clusapi/PCLUS_NETNAME_IP_INFO_FOR_MULTICHANNEL
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
 - CLUS_NETNAME_IP_INFO_FOR_MULTICHANNEL
---

# CLUS_NETNAME_IP_INFO_FOR_MULTICHANNEL structure


## -description

Represents IP information for a NetName resource that has Multichannel enabled.

## -struct-fields

### -field szName

An array of wide characters that specifies the name of the resource.

### -field NumEntries

The number of channels that are specified by the <i>IpInfo</i> parameter.

### -field IpInfo

An array of <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clus_netname_ip_info_entry">CLUS_NETNAME_IP_INFO_ENTRY</a> structures that specify the IP info for each channel.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/utility-structures">Utility structures</a>