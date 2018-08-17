---
UID: NC:clusapi.PCLUSAPI_DELETE_CLUSTER_RESOURCE_TYPE
title: PCLUSAPI_DELETE_CLUSTER_RESOURCE_TYPE
author: windows-sdk-content
description: Removes a resource type from a cluster.
old-location: mscs\deleteclusterresourcetype.htm
old-project: mscs
ms.assetid: 39615efe-e0fe-4e7b-b6f0-ba4a79d841a8
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: PCLUSAPI_DELETE_CLUSTER_RESOURCE_TYPE, PCLUSAPI_DELETE_CLUSTER_RESOURCE_TYPE callback, PCLUSAPI_DELETE_CLUSTER_RESOURCE_TYPE callback function [Failover Cluster], _wolf_deleteclusterresourcetype, clusapi/PCLUSAPI_DELETE_CLUSTER_RESOURCE_TYPE, mscs.deleteclusterresourcetype
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
tech.root: 
req.typenames: Sources
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ClusAPI.h
api_name:
 - PCLUSAPI_DELETE_CLUSTER_RESOURCE_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_DELETE_CLUSTER_RESOURCE_TYPE callback function


## -description


Removes a  <a href="https://msdn.microsoft.com/en-us/library/Aa372279(v=VS.85).aspx">resource type</a> from a <a href="https://msdn.microsoft.com/en-us/library/Aa369114(v=VS.85).aspx">cluster</a>. The <b>PCLUSAPI_DELETE_CLUSTER_RESOURCE_TYPE</b> type defines a pointer to this function.


## -parameters




### -param hCluster [in]

Handle to the cluster containing the resource type to be removed.


### -param lpszResourceTypeName [in]

Pointer to a null-terminated Unicode string containing the name of the resource type to be removed.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/en-us/library/ms681381(v=VS.85).aspx">system error code</a>.




## -remarks



The  <i>DeleteClusterResourceType</i> function only removes the resource type with the name pointed to by <i>lpszResourceTypeName</i> from the  <a href="https://msdn.microsoft.com/en-us/library/Aa369094(v=VS.85).aspx">cluster database</a> and then unregisters it with the  <a href="https://msdn.microsoft.com/en-us/library/Aa369163(v=VS.85).aspx">Cluster service</a>. The caller must delete the  <a href="https://msdn.microsoft.com/en-us/library/Aa372239(v=VS.85).aspx">resource DLL</a> for the resource type from each  <a href="https://msdn.microsoft.com/en-us/library/Aa371745(v=VS.85).aspx">node</a> in the cluster.

The caller must also delete any  <a href="https://msdn.microsoft.com/en-us/library/Aa372152(v=VS.85).aspx">resources</a> of this type before calling  <i>DeleteClusterResourceType</i> to delete the type. If any resources of the specified type still exist when  <i>DeleteClusterResourceType</i> is called, the function fails.




## -see-also




<a href="https://msdn.microsoft.com/19b8e8cf-898c-4df5-959c-e3789b082a76">CreateClusterResourceType</a>
 

 

