---
UID: NE:msclus.CLUSTER_CHANGE_SHARED_VOLUME_V2
title: CLUSTER_CHANGE_SHARED_VOLUME_V2
author: windows-sdk-content
description: Defines the notifications that are generated for a cluster shared volume.
old-location: mscs\cluster_change_shared_volume_v2.htm
old-project: mscs
ms.assetid: 2934115D-B52B-4289-9BCD-E66A4F363AE8
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: CLUSTER_CHANGE_SHARED_VOLUME_ADDED_V2, CLUSTER_CHANGE_SHARED_VOLUME_ALL_V2, CLUSTER_CHANGE_SHARED_VOLUME_REMOVED_V2, CLUSTER_CHANGE_SHARED_VOLUME_STATE_V2, CLUSTER_CHANGE_SHARED_VOLUME_V2, CLUSTER_CHANGE_SHARED_VOLUME_V2 enumeration [Failover Cluster], clusapi/CLUSTER_CHANGE_SHARED_VOLUME_ADDED_V2, clusapi/CLUSTER_CHANGE_SHARED_VOLUME_ALL_V2, clusapi/CLUSTER_CHANGE_SHARED_VOLUME_REMOVED_V2, clusapi/CLUSTER_CHANGE_SHARED_VOLUME_STATE_V2, clusapi/CLUSTER_CHANGE_SHARED_VOLUME_V2, msclus/CLUSTER_CHANGE_SHARED_VOLUME_ADDED_V2, msclus/CLUSTER_CHANGE_SHARED_VOLUME_ALL_V2, msclus/CLUSTER_CHANGE_SHARED_VOLUME_REMOVED_V2, msclus/CLUSTER_CHANGE_SHARED_VOLUME_STATE_V2, msclus/CLUSTER_CHANGE_SHARED_VOLUME_V2, mscs.cluster_change_shared_volume_v2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: msclus.h
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
req.typenames: CLUSTER_CHANGE_SHARED_VOLUME_V2
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
 - MsClus.h
api_name:
 - CLUSTER_CHANGE_SHARED_VOLUME_V2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# CLUSTER_CHANGE_SHARED_VOLUME_V2 enumeration


## -description


Defines the notifications that are generated for a cluster shared volume.


## -enum-fields




### -field CLUSTER_CHANGE_SHARED_VOLUME_STATE_V2

Indicates that the state of the cluster shared volume has changed.


### -field CLUSTER_CHANGE_SHARED_VOLUME_ADDED_V2

Indicates that the cluster shared volume was added.


### -field CLUSTER_CHANGE_SHARED_VOLUME_REMOVED_V2

Indicates that the cluster shared volume was removed.


### -field CLUSTER_CHANGE_SHARED_VOLUME_ALL_V2

Indicates all V2 cluster shared volume notifications.


## -remarks



Protocol version 2.0 servers do not support this enumeration.



