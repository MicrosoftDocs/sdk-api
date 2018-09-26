---
UID: NS:clusapi._SR_RESOURCE_TYPE_QUERY_ELIGIBLE_LOGDISKS
title: "_SR_RESOURCE_TYPE_QUERY_ELIGIBLE_LOGDISKS"
author: windows-sdk-content
description: Describes a set of retrieved disks that can be used as log disks for the specified data disk.
old-location: mscs\sr_resource_type_query_eligible_logdisks.htm
tech.root: mscs
ms.assetid: AF4EBA1C-8DAB-46F4-A092-F196F02480EB
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: "*PSR_RESOURCE_TYPE_QUERY_ELIGIBLE_LOGDISKS, PSR_RESOURCE_TYPE_QUERY_ELIGIBLE_LOGDISKS, PSR_RESOURCE_TYPE_QUERY_ELIGIBLE_LOGDISKS structure pointer [Failover Cluster], SR_RESOURCE_TYPE_QUERY_ELIGIBLE_LOGDISKS, SR_RESOURCE_TYPE_QUERY_ELIGIBLE_LOGDISKS structure [Failover Cluster], _SR_RESOURCE_TYPE_QUERY_ELIGIBLE_LOGDISKS, clusapi/PSR_RESOURCE_TYPE_QUERY_ELIGIBLE_LOGDISKS, clusapi/SR_RESOURCE_TYPE_QUERY_ELIGIBLE_LOGDISKS, mscs.sr_resource_type_query_eligible_logdisks"
ms.prod: windows
ms.technology: windows-sdk
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
 - SR_RESOURCE_TYPE_QUERY_ELIGIBLE_LOGDISKS
product: Windows
targetos: Windows
req.typenames: SR_RESOURCE_TYPE_QUERY_ELIGIBLE_LOGDISKS, *PSR_RESOURCE_TYPE_QUERY_ELIGIBLE_LOGDISKS
req.redist: 
---

# _SR_RESOURCE_TYPE_QUERY_ELIGIBLE_LOGDISKS structure


## -description


Describes a set of retrieved disks that can be used as log disks for the specified data disk.This is a data structure for a value list that is returned by the <a href="https://msdn.microsoft.com/C0D7B513-27F5-4BAC-81E2-6B8290DBAAB9">CLUSCTL_RESOURCE_TYPE_REPLICATION_GET_ELIGIBLE_LOGDISKS</a> control code.


## -struct-fields




### -field DataDiskGuid

The cluster resource identifier of the data disk.


### -field IncludeOfflineDisks

When <b>TRUE</b>, the result set includes all the offline disks in the available storage group.


## -see-also




<a href="https://msdn.microsoft.com/e3ad7c34-0c8a-4f03-8e5c-b57802c493f0">Data Structures</a>
 

 

