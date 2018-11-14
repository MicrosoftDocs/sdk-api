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


Creates a <a href="https://msdn.microsoft.com/en-us/library/Aa372279(v=VS.85).aspx">resource type</a> in a <a href="https://msdn.microsoft.com/en-us/library/Aa369336(v=VS.85).aspx">cluster</a>. The <b>PCLUSAPI_CREATE_CLUSTER_RESOURCE_TYPE</b> type defines a pointer to this function.


## -parameters




### -param hCluster [in]

Handle to the cluster to receive the new resource type.


### -param lpszResourceTypeName [in]

Pointer to a null-terminated Unicode string containing the name of the new resource type. The specified name must be unique within the cluster.


### -param lpszDisplayName [in]

Pointer to the  <a href="https://msdn.microsoft.com/en-us/library/Aa369356(v=VS.85).aspx">display name</a> for the new resource type. While the content of <i>lpszResourceTypeName</i> should uniquely identify the resource type on all clusters, the content of <i>lpszDisplayName</i> should be a localized friendly name for the resource suitable for displaying to administrators.


### -param lpszResourceTypeDll [in]

Pointer to the fully qualified name of the  <a href="https://msdn.microsoft.com/en-us/library/Aa372239(v=VS.85).aspx">resource DLL</a> for the new resource type or the path name relative to the Cluster directory.


### -param dwLooksAlivePollInterval [in]

Default millisecond value to be used as the poll interval needed by the new resource type's  <a href="https://msdn.microsoft.com/en-us/library/Aa370972(v=VS.85).aspx">LooksAlive</a> function. The <i>dwLooksAlivePollInterval</i> parameter is used to set the resource type's  <a href="https://msdn.microsoft.com/en-us/library/Aa372301(v=VS.85).aspx">LooksAlivePollInterval</a> property.


### -param dwIsAlivePollInterval [in]

Default millisecond value to be used as the poll interval needed by the new resource type's  <a href="https://msdn.microsoft.com/en-us/library/Aa370496(v=VS.85).aspx">IsAlive</a> function. The <i>dwIsAlivePollInterval</i> parameter is used to set the resource type's  <a href="https://msdn.microsoft.com/en-us/library/Aa372297(v=VS.85).aspx">IsAlivePollInterval</a> property.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/en-us/library/ms681381(v=VS.85).aspx">system error code</a>.




## -remarks



The  <b>CreateClusterResourceType</b> function only defines the resource type in the  <a href="https://msdn.microsoft.com/en-us/library/Aa369094(v=VS.85).aspx">cluster database</a> and registers the resource type with the  <a href="https://msdn.microsoft.com/en-us/library/Aa369163(v=VS.85).aspx">Cluster service</a>. To complete the process of installing a new resource type in a cluster, developers must install the resource DLLs and  <a href="https://msdn.microsoft.com/en-us/library/Aa369060(v=VS.85).aspx">Cluster Administrator</a> extension DLLs for the new types on each  <a href="https://msdn.microsoft.com/en-us/library/Aa371745(v=VS.85).aspx">node</a> in the cluster. Also, if Cluster Administrator will be used on systems that are not member nodes, the extension DLLs must also be installed on those systems.




## -see-also




<a href="https://msdn.microsoft.com/39615efe-e0fe-4e7b-b6f0-ba4a79d841a8">DeleteClusterResourceType</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370496(v=VS.85).aspx">IsAlive</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa372297(v=VS.85).aspx">IsAlivePollInterval</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370972(v=VS.85).aspx">LooksAlive</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa372301(v=VS.85).aspx">LooksAlivePollInterval</a>
 

 

