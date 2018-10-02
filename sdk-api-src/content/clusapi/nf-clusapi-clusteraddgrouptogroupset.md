---
UID: NF:clusapi.ClusterAddGroupToGroupSet
title: ClusterAddGroupToGroupSet function
author: windows-sdk-content
description: Adds the specified group to a groupset in the cluster.
old-location: mscs\clusteraddgrouptogroupcollection.htm
tech.root: MsCS
ms.assetid: f201dfaa-d9e6-41e0-8d22-23c073b1789d
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ClusterAddGroupToGroupSet, ClusterAddGroupToGroupSet function [Failover Cluster], PCLUSAPI_CLUSTER_ADD_GROUP_TO_GROUP_GROUPSET, PCLUSAPI_CLUSTER_ADD_GROUP_TO_GROUP_GROUPSET function [Failover Cluster], clusapi/ClusterAddGroupToGroupSet, clusapi/PCLUSAPI_CLUSTER_ADD_GROUP_TO_GROUP_GROUPSET, mscs.clusteraddgrouptogroupcollection
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: clusapi.h
req.include-header: 
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
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
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
req.typenames: 
req.redist: 
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
the function returns a <a href="https://msdn.microsoft.com/en-us/library/ms681381(v=VS.85).aspx">system error code</a>.



