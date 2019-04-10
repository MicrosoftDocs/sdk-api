---
UID: NF:clusapi.AddClusterGroupSetDependency
title: AddClusterGroupSetDependency function (clusapi.h)
author: windows-sdk-content
description: Adds a dependency between two cluster groupsets.
old-location: mscs\addclustergroupcollectiondependency.htm
tech.root: MsCS
ms.assetid: dab8cef1-475b-4d92-8f3f-e828d62bcd17
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AddClusterGroupSetDependency, AddClusterGroupSetDependency function [Failover Cluster], PCLUSAPI_ADD_CLUSTER_GROUP_GROUPSET_DEPENDENCY, PCLUSAPI_ADD_CLUSTER_GROUP_GROUPSET_DEPENDENCY function [Failover Cluster], clusapi/AddClusterGroupSetDependency, clusapi/PCLUSAPI_ADD_CLUSTER_GROUP_GROUPSET_DEPENDENCY, mscs.addclustergroupcollectiondependency
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
 - AddClusterGroupSetDependency
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AddClusterGroupSetDependency function


## -description


Adds a dependency between two cluster groupsets. A groupset can only be dependent
    on one other groupset.


## -parameters




### -param hDependentGroupSet [in]

The dependent collection


### -param hProviderGroupSet [in]

The collection <i>hDependentGroupSet</i> depends on.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.



