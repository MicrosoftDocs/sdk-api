---
UID: NE:msclus.CLUSTER_CHANGE_GROUPSET_V2
title: CLUSTER_CHANGE_GROUPSET_V2
author: windows-driver-content
description: Defines the list of notifications that are generated for a groupset.
old-location: mscs\cluster_change_collection_v2.htm
old-project: MsCS
ms.assetid: 5ad843d6-618b-4648-9c34-daf2f43adbec
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: CLUSTER_CHANGE_GROUPSET_ALL_V2, CLUSTER_CHANGE_GROUPSET_COMMON_PROPERTY_V2, CLUSTER_CHANGE_GROUPSET_DELETED_v2, CLUSTER_CHANGE_GROUPSET_DEPENDENCIES_V2, CLUSTER_CHANGE_GROUPSET_DEPENDENTS_V2, CLUSTER_CHANGE_GROUPSET_GROUP_ADDED, CLUSTER_CHANGE_GROUPSET_GROUP_REMOVED, CLUSTER_CHANGE_GROUPSET_HANDLE_CLOSE_v2, CLUSTER_CHANGE_GROUPSET_PRIVATE_PROPERTY_V2, CLUSTER_CHANGE_GROUPSET_STATE_V2, CLUSTER_CHANGE_GROUPSET_V2, CLUSTER_CHANGE_GROUPSET_V2 enumeration [Failover Cluster], clusapi/CLUSTER_CHANGE_GROUPSET_ALL_V2, clusapi/CLUSTER_CHANGE_GROUPSET_COMMON_PROPERTY_V2, clusapi/CLUSTER_CHANGE_GROUPSET_DELETED_v2, clusapi/CLUSTER_CHANGE_GROUPSET_DEPENDENCIES_V2, clusapi/CLUSTER_CHANGE_GROUPSET_DEPENDENTS_V2, clusapi/CLUSTER_CHANGE_GROUPSET_GROUP_ADDED, clusapi/CLUSTER_CHANGE_GROUPSET_GROUP_REMOVED, clusapi/CLUSTER_CHANGE_GROUPSET_HANDLE_CLOSE_v2, clusapi/CLUSTER_CHANGE_GROUPSET_PRIVATE_PROPERTY_V2, clusapi/CLUSTER_CHANGE_GROUPSET_STATE_V2, clusapi/CLUSTER_CHANGE_GROUPSET_V2, msclus/CLUSTER_CHANGE_GROUPSET_ALL_V2, msclus/CLUSTER_CHANGE_GROUPSET_COMMON_PROPERTY_V2, msclus/CLUSTER_CHANGE_GROUPSET_DELETED_v2, msclus/CLUSTER_CHANGE_GROUPSET_DEPENDENCIES_V2, msclus/CLUSTER_CHANGE_GROUPSET_DEPENDENTS_V2, msclus/CLUSTER_CHANGE_GROUPSET_GROUP_ADDED, msclus/CLUSTER_CHANGE_GROUPSET_GROUP_REMOVED, msclus/CLUSTER_CHANGE_GROUPSET_HANDLE_CLOSE_v2, msclus/CLUSTER_CHANGE_GROUPSET_PRIVATE_PROPERTY_V2, msclus/CLUSTER_CHANGE_GROUPSET_STATE_V2, msclus/CLUSTER_CHANGE_GROUPSET_V2, mscs.cluster_change_collection_v2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: msclus.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2016
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: CLUSTER_CHANGE_GROUPSET_V2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ClusAPI.h
-	MSClus.h
api_name:
-	CLUSTER_CHANGE_GROUPSET_V2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# CLUSTER_CHANGE_GROUPSET_V2 enumeration


## -description


Defines the list of notifications that are generated for a groupset.


## -enum-fields




### -field CLUSTER_CHANGE_GROUPSET_DELETED_v2

Indicates that a groupset was deleted.


### -field CLUSTER_CHANGE_GROUPSET_COMMON_PROPERTY_V2

Indicates that a common property of the groupset has changed.


### -field CLUSTER_CHANGE_GROUPSET_PRIVATE_PROPERTY_V2

Indicates that a private property of the groupset has changed.


### -field CLUSTER_CHANGE_GROUPSET_STATE_V2

Indicates that the group's state changed.


### -field CLUSTER_CHANGE_GROUPSET_GROUP_ADDED

Indicates that a group has been added to the groupset.


### -field CLUSTER_CHANGE_GROUPSET_GROUP_REMOVED

Indicates that a group has been removed from the groupset.


### -field CLUSTER_CHANGE_GROUPSET_DEPENDENCIES_V2

Indicates that the groupset's dependencies have changed.


### -field CLUSTER_CHANGE_GROUPSET_DEPENDENTS_V2

Indicates that the groupset's dependents have changed.


### -field CLUSTER_CHANGE_GROUPSET_HANDLE_CLOSE_v2

Indicates that the group's context handle was closed.


### -field CLUSTER_CHANGE_GROUPSET_ALL_V2

