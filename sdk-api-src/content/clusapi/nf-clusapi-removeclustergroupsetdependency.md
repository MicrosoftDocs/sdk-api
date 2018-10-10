---
UID: NF:clusapi.RemoveClusterGroupSetDependency
title: RemoveClusterGroupSetDependency function
author: windows-sdk-content
description: Removes a groupset from a groupset's dependency expression.
old-location: mscs\removeclustergroupcollectiondependency.htm
tech.root: MsCS
ms.assetid: 1a9dcc3f-e73a-4f14-a418-b1c62a0c98c2
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: PCLUSAPI_REMOVE_CLUSTER_GROUP_GROUPSET_DEPENDENCY, PCLUSAPI_REMOVE_CLUSTER_GROUP_GROUPSET_DEPENDENCY function [Failover Cluster], RemoveClusterGroupSetDependency, RemoveClusterGroupSetDependency function [Failover Cluster], clusapi/PCLUSAPI_REMOVE_CLUSTER_GROUP_GROUPSET_DEPENDENCY, clusapi/RemoveClusterGroupSetDependency, mscs.removeclustergroupcollectiondependency
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
 - RemoveClusterGroupSetDependency
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RemoveClusterGroupSetDependency function


## -description


Removes a groupset from a groupset's dependency expression.


## -parameters




### -param hGroupSet [in]

The groupset from which to remove the dependency.


### -param hDependsOn [in]

The collection to remove


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.



