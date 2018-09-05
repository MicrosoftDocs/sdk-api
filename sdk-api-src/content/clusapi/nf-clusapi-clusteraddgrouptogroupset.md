---
UID: NF:clusapi.ClusterAddGroupToGroupSet
title: ClusterAddGroupToGroupSet function
author: windows-sdk-content
description: Adds the specified group to a groupset in the cluster.
old-location: mscs\clusteraddgrouptogroupcollection.htm
old-project: mscs
ms.assetid: f201dfaa-d9e6-41e0-8d22-23c073b1789d
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ClusterAddGroupToGroupSet, ClusterAddGroupToGroupSet function [Failover Cluster], PCLUSAPI_CLUSTER_ADD_GROUP_TO_GROUP_GROUPSET, PCLUSAPI_CLUSTER_ADD_GROUP_TO_GROUP_GROUPSET function [Failover Cluster], clusapi/ClusterAddGroupToGroupSet, clusapi/PCLUSAPI_CLUSTER_ADD_GROUP_TO_GROUP_GROUPSET, mscs.clusteraddgrouptogroupcollection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: clusapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2016
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
req.typenames: SR_REPLICATED_DISK_TYPE, *PSR_REPLICATED_DISK_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
api_name:
 - ClusterAddGroupToGroupSet
product: Windows
targetos: Windows
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
---

# ClusterAddGroupToGroupSet function


## -description


Adds the specified group to a groupset in the cluster. The group
    must not currently be in a groupset


## -parameters




### -param hGroupSet [in]

The collection to which to add the group


### -param hGroup [in]

The group to add to the collection


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.



