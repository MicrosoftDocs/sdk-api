---
UID: NF:clusapi.CreateClusterResourceType
title: CreateClusterResourceType function
author: windows-sdk-content
description: Creates a resource type in a cluster.
old-location: mscs\createclusterresourcetype.htm
tech.root: mscs
ms.assetid: 19b8e8cf-898c-4df5-959c-e3789b082a76
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: CreateClusterResourceType, CreateClusterResourceType function [Failover Cluster], PCLUSAPI_CREATE_CLUSTER_RESOURCE_TYPE, PCLUSAPI_CREATE_CLUSTER_RESOURCE_TYPE function [Failover Cluster], _wolf_createclusterresourcetype, clusapi/CreateClusterResourceType, clusapi/PCLUSAPI_CREATE_CLUSTER_RESOURCE_TYPE, mscs.createclusterresourcetype
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
 - CreateClusterResourceType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- CreateClusterResourceType
: 
---

# CreateClusterResourceType function


## -description


Creates a <a href="https://msdn.microsoft.com/d02e4f51-7b86-451a-a51c-ea850ae464d1">resource type</a> in a <a href="c_gly.htm">cluster</a>. The <b>PCLUSAPI_CREATE_CLUSTER_RESOURCE_TYPE</b> type defines a pointer to this function.


## -parameters




### -param hCluster [in]

Handle to the cluster to receive the new resource type.


### -param lpszResourceTypeName [in]

Pointer to a null-terminated Unicode string containing the name of the new resource type. The specified name must be unique within the cluster.


### -param lpszDisplayName [in]

Pointer to the  <a href="https://msdn.microsoft.com/02c61e81-486c-4543-b345-a1b2dde41982">display name</a> for the new resource type. While the content of <i>lpszResourceTypeName</i> should uniquely identify the resource type on all clusters, the content of <i>lpszDisplayName</i> should be a localized friendly name for the resource suitable for displaying to administrators.


### -param lpszResourceTypeDll [in]

Pointer to the fully qualified name of the  <a href="https://msdn.microsoft.com/e1434102-afaf-4a35-887e-a434c628bd90">resource DLL</a> for the new resource type or the path name relative to the Cluster directory.


### -param dwLooksAlivePollInterval [in]

Default millisecond value to be used as the poll interval needed by the new resource type's  <a href="https://msdn.microsoft.com/cfc57325-847d-4f59-bee8-6a02b0a2ef32">LooksAlive</a> function. The <i>dwLooksAlivePollInterval</i> parameter is used to set the resource type's  <a href="https://msdn.microsoft.com/87ce50aa-a707-4091-9c65-ffdc314bcc4d">LooksAlivePollInterval</a> property.


### -param dwIsAlivePollInterval [in]

Default millisecond value to be used as the poll interval needed by the new resource type's  <a href="https://msdn.microsoft.com/ff7661af-0a24-4a2e-bb31-c967845a4ff4">IsAlive</a> function. The <i>dwIsAlivePollInterval</i> parameter is used to set the resource type's  <a href="https://msdn.microsoft.com/8d0d8dc5-0996-4775-9c19-563f345affbe">IsAlivePollInterval</a> property.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -remarks



The  <b>CreateClusterResourceType</b> function only defines the resource type in the  <a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">cluster database</a> and registers the resource type with the  <a href="https://msdn.microsoft.com/90717d6e-f2a4-49a0-86b6-17de1c4bcfe4">Cluster service</a>. To complete the process of installing a new resource type in a cluster, developers must install the resource DLLs and  <a href="https://msdn.microsoft.com/5d89c4b8-0554-4672-9e06-2ce7c5d15d5f">Cluster Administrator</a> extension DLLs for the new types on each  <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a> in the cluster. Also, if Cluster Administrator will be used on systems that are not member nodes, the extension DLLs must also be installed on those systems.




## -see-also




<a href="https://msdn.microsoft.com/39615efe-e0fe-4e7b-b6f0-ba4a79d841a8">DeleteClusterResourceType</a>



<a href="https://msdn.microsoft.com/ff7661af-0a24-4a2e-bb31-c967845a4ff4">IsAlive</a>



<a href="https://msdn.microsoft.com/8d0d8dc5-0996-4775-9c19-563f345affbe">IsAlivePollInterval</a>



<a href="https://msdn.microsoft.com/cfc57325-847d-4f59-bee8-6a02b0a2ef32">LooksAlive</a>



<a href="https://msdn.microsoft.com/87ce50aa-a707-4091-9c65-ffdc314bcc4d">LooksAlivePollInterval</a>
 

 

