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

# CLUSTER_MGMT_POINT_TYPE enumeration


## -description


Specifies the type of the management point for the cluster.

<b>CLUSTER_MGMT_POINT_TYPE</b> is used as a possible value in the <a href="https://msdn.microsoft.com/672a1573-63e5-4321-a049-25bdafc1b5e0">CreateCluster</a> configuration structure.


## -enum-fields




### -field CLUSTER_MGMT_POINT_TYPE_NONE

The cluster has no management point.


### -field CLUSTER_MGMT_POINT_TYPE_CNO

The management point is a cluster name object.


### -field CLUSTER_MGMT_POINT_TYPE_DNS_ONLY

The management point is DNS only.


### -field CLUSTER_MGMT_POINT_TYPE_CNO_ONLY

The management point type is cluster name object (CNO) only.

<b>Windows Server 2012 R2:  </b>This value is not supported before Windows Server 2016.


## -see-also




<a href="https://msdn.microsoft.com/9c2bc2ca-41e5-4e07-a3a2-d762ea5565e1">CLUSTER_IP_ENTRY</a>



<a href="https://msdn.microsoft.com/672a1573-63e5-4321-a049-25bdafc1b5e0">CreateCluster</a>



<a href="https://msdn.microsoft.com/45da8dbc-dd70-4f95-b933-66d8e4340448">Utility structures</a>
 

 

