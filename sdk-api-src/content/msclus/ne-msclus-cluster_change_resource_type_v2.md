---
UID: NE:msclus.CLUSTER_CHANGE_RESOURCE_TYPE_V2
title: CLUSTER_CHANGE_RESOURCE_TYPE_V2 (msclus.h)
description: Defines the set of notifications that are generated for a resource type.
helpviewer_keywords: ["CLUSTER_CHANGE_RESOURCE_TYPE_ALL_V2","CLUSTER_CHANGE_RESOURCE_TYPE_COMMON_PROPERTY_V2","CLUSTER_CHANGE_RESOURCE_TYPE_DELETED_V2","CLUSTER_CHANGE_RESOURCE_TYPE_DLL_UPGRADED_V2","CLUSTER_CHANGE_RESOURCE_TYPE_POSSIBLE_OWNERS_V2","CLUSTER_CHANGE_RESOURCE_TYPE_PRIVATE_PROPERTY_V2","CLUSTER_CHANGE_RESOURCE_TYPE_V2","CLUSTER_CHANGE_RESOURCE_TYPE_V2 enumeration [Failover Cluster]","CLUSTER_RESOURCE_TYPE_SPECIFIC_V2","clusapi/CLUSTER_CHANGE_RESOURCE_TYPE_ALL_V2","clusapi/CLUSTER_CHANGE_RESOURCE_TYPE_COMMON_PROPERTY_V2","clusapi/CLUSTER_CHANGE_RESOURCE_TYPE_DELETED_V2","clusapi/CLUSTER_CHANGE_RESOURCE_TYPE_DLL_UPGRADED_V2","clusapi/CLUSTER_CHANGE_RESOURCE_TYPE_POSSIBLE_OWNERS_V2","clusapi/CLUSTER_CHANGE_RESOURCE_TYPE_PRIVATE_PROPERTY_V2","clusapi/CLUSTER_CHANGE_RESOURCE_TYPE_V2","clusapi/CLUSTER_RESOURCE_TYPE_SPECIFIC_V2","msclus/CLUSTER_CHANGE_RESOURCE_TYPE_ALL_V2","msclus/CLUSTER_CHANGE_RESOURCE_TYPE_COMMON_PROPERTY_V2","msclus/CLUSTER_CHANGE_RESOURCE_TYPE_DELETED_V2","msclus/CLUSTER_CHANGE_RESOURCE_TYPE_DLL_UPGRADED_V2","msclus/CLUSTER_CHANGE_RESOURCE_TYPE_POSSIBLE_OWNERS_V2","msclus/CLUSTER_CHANGE_RESOURCE_TYPE_PRIVATE_PROPERTY_V2","msclus/CLUSTER_CHANGE_RESOURCE_TYPE_V2","msclus/CLUSTER_RESOURCE_TYPE_SPECIFIC_V2","mscs.cluster_change_resource_type_v2"]
old-location: mscs\cluster_change_resource_type_v2.htm
tech.root: MsCS
ms.assetid: 2A49AA32-F1E2-4810-B093-F6EC050DA841
ms.date: 12/05/2018
ms.keywords: CLUSTER_CHANGE_RESOURCE_TYPE_ALL_V2, CLUSTER_CHANGE_RESOURCE_TYPE_COMMON_PROPERTY_V2, CLUSTER_CHANGE_RESOURCE_TYPE_DELETED_V2, CLUSTER_CHANGE_RESOURCE_TYPE_DLL_UPGRADED_V2, CLUSTER_CHANGE_RESOURCE_TYPE_POSSIBLE_OWNERS_V2, CLUSTER_CHANGE_RESOURCE_TYPE_PRIVATE_PROPERTY_V2, CLUSTER_CHANGE_RESOURCE_TYPE_V2, CLUSTER_CHANGE_RESOURCE_TYPE_V2 enumeration [Failover Cluster], CLUSTER_RESOURCE_TYPE_SPECIFIC_V2, clusapi/CLUSTER_CHANGE_RESOURCE_TYPE_ALL_V2, clusapi/CLUSTER_CHANGE_RESOURCE_TYPE_COMMON_PROPERTY_V2, clusapi/CLUSTER_CHANGE_RESOURCE_TYPE_DELETED_V2, clusapi/CLUSTER_CHANGE_RESOURCE_TYPE_DLL_UPGRADED_V2, clusapi/CLUSTER_CHANGE_RESOURCE_TYPE_POSSIBLE_OWNERS_V2, clusapi/CLUSTER_CHANGE_RESOURCE_TYPE_PRIVATE_PROPERTY_V2, clusapi/CLUSTER_CHANGE_RESOURCE_TYPE_V2, clusapi/CLUSTER_RESOURCE_TYPE_SPECIFIC_V2, msclus/CLUSTER_CHANGE_RESOURCE_TYPE_ALL_V2, msclus/CLUSTER_CHANGE_RESOURCE_TYPE_COMMON_PROPERTY_V2, msclus/CLUSTER_CHANGE_RESOURCE_TYPE_DELETED_V2, msclus/CLUSTER_CHANGE_RESOURCE_TYPE_DLL_UPGRADED_V2, msclus/CLUSTER_CHANGE_RESOURCE_TYPE_POSSIBLE_OWNERS_V2, msclus/CLUSTER_CHANGE_RESOURCE_TYPE_PRIVATE_PROPERTY_V2, msclus/CLUSTER_CHANGE_RESOURCE_TYPE_V2, msclus/CLUSTER_RESOURCE_TYPE_SPECIFIC_V2, mscs.cluster_change_resource_type_v2
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CLUSTER_CHANGE_RESOURCE_TYPE_V2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSTER_CHANGE_RESOURCE_TYPE_V2
 - msclus/CLUSTER_CHANGE_RESOURCE_TYPE_V2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
 - MsClus.h
api_name:
 - CLUSTER_CHANGE_RESOURCE_TYPE_V2
---

# CLUSTER_CHANGE_RESOURCE_TYPE_V2 enumeration


## -description

Defines the set of notifications that are generated for a resource type.

## -enum-fields

### -field CLUSTER_CHANGE_RESOURCE_TYPE_DELETED_V2:0x1

Indicates that the resource type has been deleted.

### -field CLUSTER_CHANGE_RESOURCE_TYPE_COMMON_PROPERTY_V2:0x2

Indicates that the resource type common properties have changed.

### -field CLUSTER_CHANGE_RESOURCE_TYPE_PRIVATE_PROPERTY_V2:0x4

Indicates that the resource type private properties have changed.

### -field CLUSTER_CHANGE_RESOURCE_TYPE_POSSIBLE_OWNERS_V2:0x8

Indicates that the possible owners for the resource type have changed.

### -field CLUSTER_CHANGE_RESOURCE_TYPE_DLL_UPGRADED_V2:0x10

Indicates that the resource type DLL has been upgraded.

### -field CLUSTER_RESOURCE_TYPE_SPECIFIC_V2:0x20

An indication that is specific to the resource type.

<b>Windows Server 2012 R2 and Windows Server 2012:  </b>This member is not supported until Windows Server 2016.

### -field CLUSTER_CHANGE_RESOURCE_TYPE_ALL_V2

Indicates all V2 resource type notifications.

