---
UID: NF:clusapi.AddClusterGroupSetDependency
title: AddClusterGroupSetDependency function
author: windows-sdk-content
description: Adds a dependency between two cluster groupsets.
old-location: mscs\addclustergroupcollectiondependency.htm
old-project: mscs
ms.assetid: dab8cef1-475b-4d92-8f3f-e828d62bcd17
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: AddClusterGroupSetDependency, AddClusterGroupSetDependency function [Failover Cluster], PCLUSAPI_ADD_CLUSTER_GROUP_GROUPSET_DEPENDENCY, PCLUSAPI_ADD_CLUSTER_GROUP_GROUPSET_DEPENDENCY function [Failover Cluster], clusapi/AddClusterGroupSetDependency, clusapi/PCLUSAPI_ADD_CLUSTER_GROUP_GROUPSET_DEPENDENCY, mscs.addclustergroupcollectiondependency
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
 - AddClusterGroupSetDependency
product: Windows
targetos: Windows
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
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
the function returns a <a href="https://msdn.microsoft.com/en-us/library/ms681381(v=VS.85).aspx">system error code</a>.



