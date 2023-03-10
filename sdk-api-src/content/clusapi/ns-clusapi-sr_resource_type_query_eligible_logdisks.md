---
UID: NS:clusapi._SR_RESOURCE_TYPE_QUERY_ELIGIBLE_LOGDISKS
title: SR_RESOURCE_TYPE_QUERY_ELIGIBLE_LOGDISKS (clusapi.h)
description: Describes a set of retrieved disks that can be used as log disks for the specified data disk.
helpviewer_keywords: ["*PSR_RESOURCE_TYPE_QUERY_ELIGIBLE_LOGDISKS","PSR_RESOURCE_TYPE_QUERY_ELIGIBLE_LOGDISKS","PSR_RESOURCE_TYPE_QUERY_ELIGIBLE_LOGDISKS structure pointer [Failover Cluster]","SR_RESOURCE_TYPE_QUERY_ELIGIBLE_LOGDISKS","SR_RESOURCE_TYPE_QUERY_ELIGIBLE_LOGDISKS structure [Failover Cluster]","clusapi/PSR_RESOURCE_TYPE_QUERY_ELIGIBLE_LOGDISKS","clusapi/SR_RESOURCE_TYPE_QUERY_ELIGIBLE_LOGDISKS","mscs.sr_resource_type_query_eligible_logdisks"]
old-location: mscs\sr_resource_type_query_eligible_logdisks.htm
tech.root: MsCS
ms.assetid: AF4EBA1C-8DAB-46F4-A092-F196F02480EB
ms.date: 12/05/2018
ms.keywords: '*PSR_RESOURCE_TYPE_QUERY_ELIGIBLE_LOGDISKS, PSR_RESOURCE_TYPE_QUERY_ELIGIBLE_LOGDISKS, PSR_RESOURCE_TYPE_QUERY_ELIGIBLE_LOGDISKS structure pointer [Failover Cluster], SR_RESOURCE_TYPE_QUERY_ELIGIBLE_LOGDISKS, SR_RESOURCE_TYPE_QUERY_ELIGIBLE_LOGDISKS structure [Failover Cluster], clusapi/PSR_RESOURCE_TYPE_QUERY_ELIGIBLE_LOGDISKS, clusapi/SR_RESOURCE_TYPE_QUERY_ELIGIBLE_LOGDISKS, mscs.sr_resource_type_query_eligible_logdisks'
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
targetos: Windows
req.typenames: SR_RESOURCE_TYPE_QUERY_ELIGIBLE_LOGDISKS, *PSR_RESOURCE_TYPE_QUERY_ELIGIBLE_LOGDISKS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SR_RESOURCE_TYPE_QUERY_ELIGIBLE_LOGDISKS
 - clusapi/_SR_RESOURCE_TYPE_QUERY_ELIGIBLE_LOGDISKS
 - PSR_RESOURCE_TYPE_QUERY_ELIGIBLE_LOGDISKS
 - clusapi/PSR_RESOURCE_TYPE_QUERY_ELIGIBLE_LOGDISKS
 - SR_RESOURCE_TYPE_QUERY_ELIGIBLE_LOGDISKS
 - clusapi/SR_RESOURCE_TYPE_QUERY_ELIGIBLE_LOGDISKS
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
 - SR_RESOURCE_TYPE_QUERY_ELIGIBLE_LOGDISKS
---

# SR_RESOURCE_TYPE_QUERY_ELIGIBLE_LOGDISKS structure


## -description

Describes a set of retrieved disks that can be used as log disks for the specified data disk.This is a data structure for a value list that is returned by the <a href="/previous-versions/windows/desktop/mscs/clusctl-resource-type-replication-get-eligible-logdisks">CLUSCTL_RESOURCE_TYPE_REPLICATION_GET_ELIGIBLE_LOGDISKS</a> control code.

## -struct-fields

### -field DataDiskGuid

The cluster resource identifier of the data disk.

### -field IncludeOfflineDisks

When <b>TRUE</b>, the result set includes all the offline disks in the available storage group.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/data-structures">Data Structures</a>