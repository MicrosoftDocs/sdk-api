---
UID: NF:clusapi.RemoveClusterResourceDependency
title: RemoveClusterResourceDependency function (clusapi.h)
author: windows-sdk-content
description: Removes a dependency relationship between two resources.
old-location: mscs\removeclusterresourcedependency.htm
tech.root: MsCS
ms.assetid: 3640ad8d-db0d-4e55-bff0-35fb5d26776f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PCLUSAPI_REMOVE_CLUSTER_RESOURCE_DEPENDENCY, PCLUSAPI_REMOVE_CLUSTER_RESOURCE_DEPENDENCY function [Failover Cluster], RemoveClusterResourceDependency, RemoveClusterResourceDependency function [Failover Cluster], _wolf_removeclusterresourcedependency, clusapi/PCLUSAPI_REMOVE_CLUSTER_RESOURCE_DEPENDENCY, clusapi/RemoveClusterResourceDependency, mscs.removeclusterresourcedependency
ms.topic: function
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
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
 - Ext-MS-Win-Cluster-ClusAPI-L1-1-2.dll
api_name:
 - RemoveClusterResourceDependency
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RemoveClusterResourceDependency function


## -description


Removes a  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/resource-dependencies">dependency</a> relationship between two  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/resources">resources</a>. The <b>PCLUSAPI_REMOVE_CLUSTER_RESOURCE_DEPENDENCY</b> type defines a pointer to this function.


## -parameters




### -param hResource [in]

Handle to the dependent resource.


### -param hDependsOn [in]

Handle to the resource that the resource identified by <i>hResource</i> currently depends on.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error code</a>.




## -remarks



Do not call  <b>RemoveClusterResourceDependency</b> from a resource DLL. For more information, see  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/function-calls-to-avoid-in-resource-dlls">Function Calls to Avoid in Resource DLLs</a>.

Do not pass LPC and RPC handles to the same function call. Otherwise, the call will raise an RPC exception and can have additional destructive effects. For information on how LPC and RPC handles are created, see  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/using-object-handles">Using Object Handles</a> and  <a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-opencluster">OpenCluster</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-addclusterresourcedependency">AddClusterResourceDependency</a>



<a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-canresourcebedependent">CanResourceBeDependent</a>



<a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-opencluster">OpenCluster</a>



<a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-openclusterresource">OpenClusterResource</a>
 

 

