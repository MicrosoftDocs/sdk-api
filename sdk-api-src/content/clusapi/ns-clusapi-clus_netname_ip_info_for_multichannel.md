---
UID: NS:clusapi.CLUS_NETNAME_IP_INFO_FOR_MULTICHANNEL
title: CLUS_NETNAME_IP_INFO_FOR_MULTICHANNEL
author: windows-sdk-content
description: Represents IP information for a NetName resource that has Multichannel enabled.
old-location: mscs\clus_netname_ip_info_for_multichannel.htm
old-project: MsCS
ms.assetid: 724FD774-00F4-4617-B761-87509AD61AF4
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: "*PCLUS_NETNAME_IP_INFO_FOR_MULTICHANNEL, CLUS_NETNAME_IP_INFO_FOR_MULTICHANNEL, CLUS_NETNAME_IP_INFO_FOR_MULTICHANNEL structure [Failover Cluster], PCLUS_NETNAME_IP_INFO_FOR_MULTICHANNEL, PCLUS_NETNAME_IP_INFO_FOR_MULTICHANNEL structure pointer [Failover Cluster], clusapi/CLUS_NETNAME_IP_INFO_FOR_MULTICHANNEL, clusapi/PCLUS_NETNAME_IP_INFO_FOR_MULTICHANNEL, mscs.clus_netname_ip_info_for_multichannel"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: CLUS_NETNAME_IP_INFO_FOR_MULTICHANNEL, *PCLUS_NETNAME_IP_INFO_FOR_MULTICHANNEL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusApi.h
api_name:
 - CLUS_NETNAME_IP_INFO_FOR_MULTICHANNEL
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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

An array of <a href="https://msdn.microsoft.com/9631BDB9-6B7C-4BFF-9654-20C77F851A22">CLUS_NETNAME_IP_INFO_ENTRY</a> structures that specify the IP info for each channel.


## -see-also




<a href="https://msdn.microsoft.com/45da8dbc-dd70-4f95-b933-66d8e4340448">Utility structures</a>
 

 

