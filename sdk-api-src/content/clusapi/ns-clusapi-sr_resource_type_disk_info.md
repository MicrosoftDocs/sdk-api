---
UID: NS:clusapi._SR_RESOURCE_TYPE_DISK_INFO
title: SR_RESOURCE_TYPE_DISK_INFO (clusapi.h)
author: windows-sdk-content
description: Describes a set of information that indicates whether a disk is eligible for replication.
old-location: mscs\sr_resource_type_disk_info.htm
tech.root: MsCS
ms.assetid: 8A53714D-D125-4B83-B51D-DF0EADE4C4E0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PSR_RESOURCE_TYPE_DISK_INFO, PSR_RESOURCE_TYPE_DISK_INFO, PSR_RESOURCE_TYPE_DISK_INFO structure pointer [Failover Cluster], SR_RESOURCE_TYPE_DISK_INFO, SR_RESOURCE_TYPE_DISK_INFO structure [Failover Cluster], clusapi/PSR_RESOURCE_TYPE_DISK_INFO, clusapi/SR_RESOURCE_TYPE_DISK_INFO, msclus/PSR_RESOURCE_TYPE_DISK_INFO, msclus/SR_RESOURCE_TYPE_DISK_INFO, mscs.sr_resource_type_disk_info"
ms.topic: struct
f1_keywords: 
 - "clusapi/SR_RESOURCE_TYPE_DISK_INFO"
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
 - MsClus.h
api_name:
 - SR_RESOURCE_TYPE_DISK_INFO
product: Windows
targetos: Windows
req.typenames: SR_RESOURCE_TYPE_DISK_INFO, *PSR_RESOURCE_TYPE_DISK_INFO
req.redist: 
ms.custom: 19H1
---

# SR_RESOURCE_TYPE_DISK_INFO structure


## -description


Describes a set of information that indicates whether a disk is eligible for replication.


## -struct-fields




### -field Reason

Indicates the reason that the disk is eligible or ineligible for replication.


### -field DiskGuid

 




#### - DiskInfo

The cluster resource identifier of the disk.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/cluster-enumerations">Failover Cluster Enumerations</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/clusapi/ns-clusapi-_sr_resource_type_eligible_disks_result">SR_RESOURCE_TYPE_ELIGIBLE_DISKS_RESULT</a>
 

 

