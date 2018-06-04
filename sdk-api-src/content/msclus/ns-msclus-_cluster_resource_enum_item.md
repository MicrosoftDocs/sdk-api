---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

