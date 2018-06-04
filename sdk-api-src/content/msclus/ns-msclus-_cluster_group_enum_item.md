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

# _CLUSTER_GROUP_ENUM_ITEM structure


## -description


Contains the properties of a cluster group. This structure  is used to enumerate cluster groups in the 
    <a href="https://msdn.microsoft.com/139FE5AB-9465-46F8-B360-F27F19D82A88">ClusterGroupEnumEx</a> function.


## -struct-fields




### -field dwVersion

The version of the 
      <b>CLUSTER_GROUP_ENUM_ITEM</b> structure.


### -field cbId

The size, in bytes, of the <b>lpszId</b> field.


### -field lpszId

The Id of the cluster group.


### -field cbName

The size, in bytes, of the <b>IpszName</b> field.


### -field lpszName

 


### -field state

The current state of the cluster group.


### -field cbOwnerNode

The size, in bytes, of the <b>IpszOwnerNode</b> field.


### -field lpszOwnerNode

 


### -field dwFlags

The group flags.


### -field cbProperties

The size, in bytes, of the <b>pProperties</b> field.


### -field pProperties

A pointer to a list of names of common properties.


### -field cbRoProperties

The size, in bytes, of the <b>pRoProperties</b> field.


### -field pRoProperties

A pointer to a list of names of read-only common properties.


#### - IpszName

The name of the cluster group.


#### - IpszOwnerNode

The name of the cluster node hosting the group.

