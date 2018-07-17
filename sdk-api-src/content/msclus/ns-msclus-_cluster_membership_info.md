---
UID: NS:msclus._CLUSTER_MEMBERSHIP_INFO
title: "_CLUSTER_MEMBERSHIP_INFO"
author: windows-sdk-content
description: Represents membership information for a cluster.
old-location: mscs\cluster_membership_info.htm
old-project: mscs
ms.assetid: 4E3F8DFF-6F32-4729-9AAC-56B3E2592393
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: "*PCLUSTER_MEMBERSHIP_INFO, CLUSTER_MEMBERSHIP_INFO, CLUSTER_MEMBERSHIP_INFO structure [Failover Cluster], PCLUSTER_MEMBERSHIP_INFO, PCLUSTER_MEMBERSHIP_INFO structure pointer [Failover Cluster], _CLUSTER_MEMBERSHIP_INFO, _CLUSTER_MEMBERSHIP_INFO structure [Failover Cluster], clusapi/CLUSTER_MEMBERSHIP_INFO, clusapi/PCLUSTER_MEMBERSHIP_INFO, clusapi/_CLUSTER_MEMBERSHIP_INFO, msclus/CLUSTER_MEMBERSHIP_INFO, msclus/PCLUSTER_MEMBERSHIP_INFO, msclus/_CLUSTER_MEMBERSHIP_INFO, mscs.cluster_membership_info"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: msclus.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: MsClus.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: MsClus.tlb
tech.root: 
req.typenames: CLUSTER_MEMBERSHIP_INFO, *PCLUSTER_MEMBERSHIP_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusApi.h
 - MsClus.h
api_name:
 - CLUSTER_MEMBERSHIP_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _CLUSTER_MEMBERSHIP_INFO structure


## -description


Represents membership information for a cluster.


## -struct-fields




### -field HasQuorum

<b>TRUE</b> if the cluster has a majority quorum; otherwise <b>FALSE</b>.


### -field UpnodesSize

The size of the <i>Upnodes</i> parameter.


### -field Upnodes

A byte array that specifies the nodes in the cluster that are online.


## -see-also




<a href="https://msdn.microsoft.com/e3ad7c34-0c8a-4f03-8e5c-b57802c493f0">Data Structures</a>
 

 

