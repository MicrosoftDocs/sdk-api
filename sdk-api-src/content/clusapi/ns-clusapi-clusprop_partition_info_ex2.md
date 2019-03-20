---
UID: NS:clusapi.CLUSPROP_PARTITION_INFO_EX2
title: CLUSPROP_PARTITION_INFO_EX2 (clusapi.h)
author: windows-sdk-content
description: A value list entry that contains partition information for a storage class resource. This structure is as a input, and a as a return value for the CLUSCTL_RESOURCE_STORAGE_GET_DISK_INFO_EX2 control code.
old-location: mscs\clusprop_partition_info_ex2.htm
tech.root: MsCS
ms.assetid: D6D26335-80D0-4949-99B4-FE18DD2FFF3C
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PCLUSPROP_PARTITION_INFO_EX2, CLUSPROP_PARTITION_INFO_EX2, CLUSPROP_PARTITION_INFO_EX2 structure [Failover Cluster], clusapi/CLUSPROP_PARTITION_INFO_EX2, mscs.clusprop_partition_info_ex2"
ms.topic: struct
req.header: clusapi.h
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
 - CLUSPROP_PARTITION_INFO_EX2
product: Windows
targetos: Windows
req.typenames: CLUSPROP_PARTITION_INFO_EX2
req.redist: 
---

# CLUSPROP_PARTITION_INFO_EX2 structure


## -description


A value list entry that contains partition information for a storage class resource. This structure is as a input, and a as a return value for the <a href="https://msdn.microsoft.com/FA742D78-D89D-472D-B5C9-6C8D95883CD1">CLUSCTL_RESOURCE_STORAGE_GET_DISK_INFO_EX2</a> control code.


## -struct-fields




### -field CLUSPROP_PARTITION_INFO_EX

A <a href="https://msdn.microsoft.com/b1343a04-b8bd-469a-a620-985eeb89401c">CLUSPROP_PARTITION_INFO_EX</a> structure that describes the format, 
     type, and length of the partition information.


### -field CLUS_PARTITION_INFO_EX2

A <a href="https://msdn.microsoft.com/1B6690DB-9D23-4D0C-98B7-3066C5452CD1">CLUS_PARTITION_INFO_EX2</a> structure that contains the values of the partition information.


## -see-also




<a href="https://msdn.microsoft.com/e3ad7c34-0c8a-4f03-8e5c-b57802c493f0">Data Structures</a>
 

 

