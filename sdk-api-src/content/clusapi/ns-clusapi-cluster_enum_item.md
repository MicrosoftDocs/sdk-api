---
UID: NS:clusapi._CLUSTER_ENUM_ITEM
title: CLUSTER_ENUM_ITEM
author: windows-sdk-content
description: Contains the properties of a cluster object. This structure is used to enumerate clusters in the ClusterEnumEx and ClusterNodeEnumEx functions.
old-location: mscs\cluster_enum_item.htm
tech.root: MsCS
ms.assetid: 2E7FB4DA-88AD-4739-ACE0-D43670F914D4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PCLUSTER_ENUM_ITEM, CLUSTER_ENUM_ITEM, CLUSTER_ENUM_ITEM structure [Failover Cluster], PCLUSTER_ENUM_ITEM, PCLUSTER_ENUM_ITEM structure pointer [Failover Cluster], _CLUSTER_ENUM_ITEM, _CLUSTER_ENUM_ITEM structure [Failover Cluster], clusapi/CLUSTER_ENUM_ITEM, clusapi/PCLUSTER_ENUM_ITEM, clusapi/_CLUSTER_ENUM_ITEM, msclus/CLUSTER_ENUM_ITEM, msclus/PCLUSTER_ENUM_ITEM, msclus/_CLUSTER_ENUM_ITEM, mscs.cluster_enum_item"
ms.topic: struct
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusApi.h
 - MSClus.h
api_name:
 - CLUSTER_ENUM_ITEM
product: Windows
targetos: Windows
req.typenames: CLUSTER_ENUM_ITEM, *PCLUSTER_ENUM_ITEM
req.redist: 
---

# CLUSTER_ENUM_ITEM structure


## -description


Contains the properties of a cluster object. This structure is used to enumerate clusters in the <a href="https://msdn.microsoft.com/F50FB801-8ACA-40BD-9E89-7E3AF2CA2DA5">ClusterEnumEx</a> and <a href="https://msdn.microsoft.com/1F3DFD5C-978B-4943-B4D8-81A7F9D7A3AF">ClusterNodeEnumEx</a> functions.


## -struct-fields




### -field dwVersion

The version of the <b>CLUSTER_ENUM_ITEM</b> structure.


### -field dwType

A bitmask that specifies the type of the cluster object.


### -field cbId

The size, in bytes, of the <b>lpszId</b> field.


### -field lpszId

The ID of the cluster.


### -field cbName

The size, in bytes, of the <b>lpszName</b> field.


### -field lpszName

The name of the cluster.


## -see-also




<a href="https://msdn.microsoft.com/F50FB801-8ACA-40BD-9E89-7E3AF2CA2DA5">ClusterEnumEx</a>



<a href="https://msdn.microsoft.com/1F3DFD5C-978B-4943-B4D8-81A7F9D7A3AF">ClusterNodeEnumEx</a>



<a href="https://msdn.microsoft.com/e3ad7c34-0c8a-4f03-8e5c-b57802c493f0">Data Structures</a>
 

 

