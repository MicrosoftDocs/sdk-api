---
UID: NF:clusapi.AddClusterGroupToGroupSetDependency
title: AddClusterGroupToGroupSetDependency function
author: windows-sdk-content
description: Adds a dependency between a cluster group and a cluster groupset.
old-location: mscs\addclustergrouptogroupcollectiondependency.htm
old-project: mscs
ms.assetid: ceb30c1f-39eb-4020-84c6-e6749f0b18a2
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: AddClusterGroupToGroupSetDependency, AddClusterGroupToGroupSetDependency function [Failover Cluster], PCLUSAPI_ADD_CLUSTER_GROUP_TO_GROUP_GROUPSET_DEPENDENCY, PCLUSAPI_ADD_CLUSTER_GROUP_TO_GROUP_GROUPSET_DEPENDENCY function [Failover Cluster], clusapi/AddClusterGroupToGroupSetDependency, clusapi/PCLUSAPI_ADD_CLUSTER_GROUP_TO_GROUP_GROUPSET_DEPENDENCY, mscs.addclustergrouptogroupcollectiondependency
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
 - AddClusterGroupToGroupSetDependency
product: Windows
targetos: Windows
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
---

# AddClusterGroupToGroupSetDependency function


## -description


Adds a dependency between a cluster group and a cluster groupset.A group can only be dependent on one groupset.


## -parameters




### -param hDependentGroup [in]

The dependent group


### -param hProviderGroupSet [in]

The collection <i>hDependentGroup</i> depends on


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.



