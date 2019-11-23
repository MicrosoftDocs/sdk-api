---
UID: NF:clusapi.AddClusterGroupToGroupSetDependency
title: AddClusterGroupToGroupSetDependency function (clusapi.h)

description: Adds a dependency between a cluster group and a cluster groupset.
old-location: mscs\addclustergrouptogroupcollectiondependency.htm
tech.root: MsCS
ms.assetid: ceb30c1f-39eb-4020-84c6-e6749f0b18a2

ms.date: 12/05/2018
ms.keywords: AddClusterGroupToGroupSetDependency, AddClusterGroupToGroupSetDependency function [Failover Cluster], PCLUSAPI_ADD_CLUSTER_GROUP_TO_GROUP_GROUPSET_DEPENDENCY, PCLUSAPI_ADD_CLUSTER_GROUP_TO_GROUP_GROUPSET_DEPENDENCY function [Failover Cluster], clusapi/AddClusterGroupToGroupSetDependency, clusapi/PCLUSAPI_ADD_CLUSTER_GROUP_TO_GROUP_GROUPSET_DEPENDENCY, mscs.addclustergrouptogroupcollectiondependency
ms.topic: function
f1_keywords: 
 - "clusapi/AddClusterGroupToGroupSetDependency"
dev_langs:
 - c++
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
 - AddClusterGroupToGroupSetDependency
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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
the function returns a <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error code</a>.



