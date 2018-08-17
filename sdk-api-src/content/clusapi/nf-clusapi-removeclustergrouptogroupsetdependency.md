---
UID: NF:clusapi.RemoveClusterGroupToGroupSetDependency
title: RemoveClusterGroupToGroupSetDependency function
author: windows-sdk-content
description: Removes a groupset from a group's dependency expression.
old-location: mscs\removeclustergrouptogroupcollectiondependency.htm
old-project: mscs
ms.assetid: 2bd7e1f4-0b88-466f-a408-dddb9a11a52d
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PCLUSAPI_REMOVE_CLUSTER_GROUP_TO_GROUP_GROUPSET_DEPENDENCY, PCLUSAPI_REMOVE_CLUSTER_GROUP_TO_GROUP_GROUPSET_DEPENDENCY function [Failover Cluster], RemoveClusterGroupToGroupSetDependency, RemoveClusterGroupToGroupSetDependency function [Failover Cluster], clusapi/PCLUSAPI_REMOVE_CLUSTER_GROUP_TO_GROUP_GROUPSET_DEPENDENCY, clusapi/RemoveClusterGroupToGroupSetDependency, mscs.removeclustergrouptogroupcollectiondependency
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
 - RemoveClusterGroupToGroupSetDependency
product: Windows
targetos: Windows
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
---

# RemoveClusterGroupToGroupSetDependency function


## -description


Removes a groupset from a group's dependency expression.


## -parameters




### -param hGroup [in]

The group from which to remove the dependency.


### -param hDependsOn [in]

The groupset to remove.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/en-us/library/ms681381(v=VS.85).aspx">system error code</a>.



