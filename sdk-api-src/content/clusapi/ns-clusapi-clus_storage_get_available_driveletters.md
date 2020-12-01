---
UID: NS:clusapi._CLUS_STORAGE_GET_AVAILABLE_DRIVELETTERS
title: CLUS_STORAGE_GET_AVAILABLE_DRIVELETTERS (clusapi.h)
description: Contains a bitmask of the driver letters that are available on a node. It is used as the return value of the CLUSCTL_RESOURCE_TYPE_STORAGE_GET_DRIVELETTERS control code.
helpviewer_keywords: ["*PCLUS_STORAGE_GET_AVAILABLE_DRIVELETTERS","CLUS_STORAGE_GET_AVAILABLE_DRIVELETTERS","CLUS_STORAGE_GET_AVAILABLE_DRIVELETTERS structure [Failover Cluster]","PCLUS_STORAGE_GET_AVAILABLE_DRIVELETTERS","PCLUS_STORAGE_GET_AVAILABLE_DRIVELETTERS structure pointer [Failover Cluster]","clusapi/CLUS_STORAGE_GET_AVAILABLE_DRIVELETTERS","clusapi/PCLUS_STORAGE_GET_AVAILABLE_DRIVELETTERS","mscs.clus_storage_get_available_driveletters"]
old-location: mscs\clus_storage_get_available_driveletters.htm
tech.root: MsCS
ms.assetid: 37a843db-bb11-46e5-9b1c-da8403f73aa6
ms.date: 12/05/2018
ms.keywords: '*PCLUS_STORAGE_GET_AVAILABLE_DRIVELETTERS, CLUS_STORAGE_GET_AVAILABLE_DRIVELETTERS, CLUS_STORAGE_GET_AVAILABLE_DRIVELETTERS structure [Failover Cluster], PCLUS_STORAGE_GET_AVAILABLE_DRIVELETTERS, PCLUS_STORAGE_GET_AVAILABLE_DRIVELETTERS structure pointer [Failover Cluster], clusapi/CLUS_STORAGE_GET_AVAILABLE_DRIVELETTERS, clusapi/PCLUS_STORAGE_GET_AVAILABLE_DRIVELETTERS, mscs.clus_storage_get_available_driveletters'
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise
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
req.typenames: CLUS_STORAGE_GET_AVAILABLE_DRIVELETTERS, *PCLUS_STORAGE_GET_AVAILABLE_DRIVELETTERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CLUS_STORAGE_GET_AVAILABLE_DRIVELETTERS
 - clusapi/_CLUS_STORAGE_GET_AVAILABLE_DRIVELETTERS
 - PCLUS_STORAGE_GET_AVAILABLE_DRIVELETTERS
 - clusapi/PCLUS_STORAGE_GET_AVAILABLE_DRIVELETTERS
 - CLUS_STORAGE_GET_AVAILABLE_DRIVELETTERS
 - clusapi/CLUS_STORAGE_GET_AVAILABLE_DRIVELETTERS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
api_name:
 - CLUS_STORAGE_GET_AVAILABLE_DRIVELETTERS
---

# CLUS_STORAGE_GET_AVAILABLE_DRIVELETTERS structure


## -description

Contains a bitmask of the driver letters that are available on  a node. It is used as the return value of the <a href="/previous-versions/windows/desktop/mscs/clusctl-resource-type-storage-get-driveletters">CLUSCTL_RESOURCE_TYPE_STORAGE_GET_DRIVELETTERS</a> control code.

## -struct-fields

### -field AvailDrivelettersMask

The least significant bit represents the letter 'A' and is set to zero if any partition on the node has that drive letter in use. This convention continues until bit 26, which represents the letter 'Z'. The value of bits 27 through 32 is not defined.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-type-storage-get-driveletters">CLUSCTL_RESOURCE_TYPE_STORAGE_GET_DRIVELETTERS</a>