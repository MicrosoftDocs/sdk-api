---
UID: NF:clusapi.DeleteClusterResourceType
title: DeleteClusterResourceType function
author: windows-sdk-content
description: Removes a resource type from a cluster.
old-location: mscs\deleteclusterresourcetype.htm
tech.root: mscs
ms.assetid: 39615efe-e0fe-4e7b-b6f0-ba4a79d841a8
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: DeleteClusterResourceType, DeleteClusterResourceType function [Failover Cluster], PCLUSAPI_DELETE_CLUSTER_RESOURCE_TYPE, PCLUSAPI_DELETE_CLUSTER_RESOURCE_TYPE function [Failover Cluster], _wolf_deleteclusterresourcetype, clusapi/DeleteClusterResourceType, clusapi/PCLUSAPI_DELETE_CLUSTER_RESOURCE_TYPE, mscs.deleteclusterresourcetype
ms.prod: windows-hardware
ms.technology: windows-devices
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
api_name:
 - DeleteClusterResourceType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DeleteClusterResourceType function


## -description


Removes a  <a href="https://msdn.microsoft.com/d02e4f51-7b86-451a-a51c-ea850ae464d1">resource type</a> from a <a href="c_gly.htm">cluster</a>. The <b>PCLUSAPI_DELETE_CLUSTER_RESOURCE_TYPE</b> type defines a pointer to this function.


## -parameters




### -param hCluster [in]

Handle to the cluster containing the resource type to be removed.


### -param lpszResourceTypeName [in]

Pointer to a null-terminated Unicode string containing the name of the resource type to be removed.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -remarks



The  <b>DeleteClusterResourceType</b> function only removes the resource type with the name pointed to by <i>lpszResourceTypeName</i> from the  <a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">cluster database</a> and then unregisters it with the  <a href="https://msdn.microsoft.com/90717d6e-f2a4-49a0-86b6-17de1c4bcfe4">Cluster service</a>. The caller must delete the  <a href="https://msdn.microsoft.com/e1434102-afaf-4a35-887e-a434c628bd90">resource DLL</a> for the resource type from each  <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a> in the cluster.

The caller must also delete any  <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resources</a> of this type before calling  <b>DeleteClusterResourceType</b> to delete the type. If any resources of the specified type still exist when  <b>DeleteClusterResourceType</b> is called, the function fails.




## -see-also




<a href="https://msdn.microsoft.com/19b8e8cf-898c-4df5-959c-e3789b082a76">CreateClusterResourceType</a>
 

 

