---
UID: NS:clusapi._CLUS_STORAGE_GET_AVAILABLE_DRIVELETTERS
title: "_CLUS_STORAGE_GET_AVAILABLE_DRIVELETTERS"
author: windows-sdk-content
description: Contains a bitmask of the driver letters that are available on a node. It is used as the return value of the CLUSCTL_RESOURCE_TYPE_STORAGE_GET_DRIVELETTERS control code.
old-location: mscs\clus_storage_get_available_driveletters.htm
tech.root: mscs
ms.assetid: 37a843db-bb11-46e5-9b1c-da8403f73aa6
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: "*PCLUS_STORAGE_GET_AVAILABLE_DRIVELETTERS, CLUS_STORAGE_GET_AVAILABLE_DRIVELETTERS, CLUS_STORAGE_GET_AVAILABLE_DRIVELETTERS structure [Failover Cluster], PCLUS_STORAGE_GET_AVAILABLE_DRIVELETTERS, PCLUS_STORAGE_GET_AVAILABLE_DRIVELETTERS structure pointer [Failover Cluster], _CLUS_STORAGE_GET_AVAILABLE_DRIVELETTERS, clusapi/CLUS_STORAGE_GET_AVAILABLE_DRIVELETTERS, clusapi/PCLUS_STORAGE_GET_AVAILABLE_DRIVELETTERS, mscs.clus_storage_get_available_driveletters"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
api_name:
 - CLUS_STORAGE_GET_AVAILABLE_DRIVELETTERS
product: Windows
targetos: Windows
req.typenames: CLUS_STORAGE_GET_AVAILABLE_DRIVELETTERS, *PCLUS_STORAGE_GET_AVAILABLE_DRIVELETTERS
req.redist: 
---

# _CLUS_STORAGE_GET_AVAILABLE_DRIVELETTERS structure


## -description


Contains a bitmask of the driver letters that are available on  a node. It is used as the return value of the <a href="https://msdn.microsoft.com/7960baea-64b5-481b-9237-044ffa7b3b0a">CLUSCTL_RESOURCE_TYPE_STORAGE_GET_DRIVELETTERS</a> control code.


## -struct-fields




### -field AvailDrivelettersMask

The least significant bit represents the letter 'A' and is set to zero if any partition on the node has that drive letter in use. This convention continues until bit 26, which represents the letter 'Z'. The value of bits 27 through 32 is not defined.


## -see-also




<a href="https://msdn.microsoft.com/7960baea-64b5-481b-9237-044ffa7b3b0a">CLUSCTL_RESOURCE_TYPE_STORAGE_GET_DRIVELETTERS</a>
 

 

