---
UID: NS:clusapi.CLUS_FORCE_QUORUM_INFO
title: CLUS_FORCE_QUORUM_INFO
author: windows-sdk-content
description: Specifies information about the list of nodes sufficient to establish quorum in a majority-of-nodes cluster.
old-location: mscs\clus_force_quorum_info.htm
tech.root: MsCS
ms.assetid: dda10d88-0e5f-40f7-b18b-82dacef6f886
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PCLUS_FORCE_QUORUM_INFO, CLUS_FORCE_QUORUM_INFO, CLUS_FORCE_QUORUM_INFO structure [Failover Cluster], PCLUS_FORCE_QUORUM_INFO, PCLUS_FORCE_QUORUM_INFO structure pointer [Failover Cluster], _wolf_clus_force_quorum_info, clusapi/CLUS_FORCE_QUORUM_INFO, clusapi/PCLUS_FORCE_QUORUM_INFO, mscs.clus_force_quorum_info"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
api_name:
 - CLUS_FORCE_QUORUM_INFO
product: Windows
targetos: Windows
req.typenames: CLUS_FORCE_QUORUM_INFO, *PCLUS_FORCE_QUORUM_INFO
req.redist: 
---

# CLUS_FORCE_QUORUM_INFO structure


## -description


Specifies information about the list of 
    <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">nodes</a> sufficient to establish quorum in a majority-of-nodes 
    cluster.


## -struct-fields




### -field dwSize

The total size of the structure, including the nodes list.


### -field dwNodeBitMask

A bit mask representing the maximum assumed node set.


### -field dwMaxNumberofNodes

The number of bits set in the mask


### -field multiszNodeList

The names of the nodes that are sufficient to establish quorum in a majority-of-nodes cluster. This list should be comma delimited with no spaces.


## -see-also




<a href="https://msdn.microsoft.com/ab957c9c-fe05-424f-80e7-48d74acca6ed">CLUSCTL_RESOURCE_FORCE_QUORUM</a>
 

 

