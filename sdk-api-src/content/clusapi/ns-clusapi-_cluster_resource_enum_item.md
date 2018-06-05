---
UID: NS:clusapi._CLUSTER_RESOURCE_ENUM_ITEM
title: "_CLUSTER_RESOURCE_ENUM_ITEM"
author: windows-sdk-content
description: Represents the properties of a cluster resource. This structure is used to enumerate cluster resources in the ClusterResourceEnumEx function.
old-location: mscs\cluster_resource_enum_item.htm
old-project: MsCS
ms.assetid: B8369B29-F72A-4642-93CB-23F04E680663
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: "*PCLUSTER_RESOURCE_ENUM_ITEM, CLUSTER_RESOURCE_ENUM_ITEM, CLUSTER_RESOURCE_ENUM_ITEM structure [Failover Cluster], PCLUSTER_RESOURCE_ENUM_ITEM, PCLUSTER_RESOURCE_ENUM_ITEM structure pointer [Failover Cluster], _CLUSTER_RESOURCE_ENUM_ITEM, _CLUSTER_RESOURCE_ENUM_ITEM structure [Failover Cluster], clusapi/CLUSTER_RESOURCE_ENUM_ITEM, clusapi/PCLUSTER_RESOURCE_ENUM_ITEM, clusapi/_CLUSTER_RESOURCE_ENUM_ITEM, msclus/CLUSTER_RESOURCE_ENUM_ITEM, msclus/PCLUSTER_RESOURCE_ENUM_ITEM, msclus/_CLUSTER_RESOURCE_ENUM_ITEM, mscs.cluster_resource_enum_item"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
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
req.typenames: CLUSTER_RESOURCE_ENUM_ITEM, *PCLUSTER_RESOURCE_ENUM_ITEM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ClusApi.h
-	MsClus.h
api_name:
-	CLUSTER_RESOURCE_ENUM_ITEM
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _CLUSTER_RESOURCE_ENUM_ITEM structure


## -description


Represents the properties of a cluster resource. This structure is used to enumerate cluster resources in the <a href="https://msdn.microsoft.com/9B5C03DF-84BB-4B3A-8404-94C64F192305">ClusterResourceEnumEx</a> function.


## -struct-fields




### -field dwVersion

 


### -field cbId

 


### -field lpszId

 


### -field cbName

The size, in bytes, of the <b>IpszName</b> field.


### -field lpszName

The name of the cluster resource.


### -field cbOwnerGroupName

The size, in bytes, of the <b>IpszOwnerNode</b> field.


### -field lpszOwnerGroupName

The name of the cluster resource that  hosts the group.


### -field cbOwnerGroupId

The size, in bytes, of the <b>lpszOwnerGroupId</b> field.


### -field lpszOwnerGroupId

The group ID of the cluster group for the resource.


### -field cbProperties

The size, in bytes, of the <b>pProperties</b> field.


### -field pProperties

A pointer to a list of names of common properties.


### -field cbRoProperties

The size, in bytes, of the <b>pRoProperties</b> field.


### -field pRoProperties

A pointer to a list of names of read-only common properties.


#### - DWORD

The version of this structure.

The size, in bytes, of the <b>lpszId</b> field.


#### - LPWSTR

The ID of the cluster resource.


## -see-also




<a href="https://msdn.microsoft.com/9B5C03DF-84BB-4B3A-8404-94C64F192305">ClusterResourceEnumEx</a>



<a href="https://msdn.microsoft.com/45da8dbc-dd70-4f95-b933-66d8e4340448">Utility structures</a>
 

 

