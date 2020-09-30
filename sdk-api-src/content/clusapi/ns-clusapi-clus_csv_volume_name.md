---
UID: NS:clusapi._CLUS_CSV_VOLUME_NAME
title: CLUS_CSV_VOLUME_NAME (clusapi.h)
description: Represents the name of a cluster shared volume (CSV).
helpviewer_keywords: ["*PCLUS_CSV_VOLUME_NAME","CLUS_CSV_VOLUME_NAME","CLUS_CSV_VOLUME_NAME structure [Failover Cluster]","PCLUS_CSV_VOLUME_NAME","PCLUS_CSV_VOLUME_NAME structure pointer [Failover Cluster]","clusapi/CLUS_CSV_VOLUME_NAME","clusapi/PCLUS_CSV_VOLUME_NAME","mscs.clus_csv_volume_name"]
old-location: mscs\clus_csv_volume_name.htm
tech.root: MsCS
ms.assetid: 18E17AA6-1244-41EA-918E-7BDBB90A0D70
ms.date: 12/05/2018
ms.keywords: '*PCLUS_CSV_VOLUME_NAME, CLUS_CSV_VOLUME_NAME, CLUS_CSV_VOLUME_NAME structure [Failover Cluster], PCLUS_CSV_VOLUME_NAME, PCLUS_CSV_VOLUME_NAME structure pointer [Failover Cluster], clusapi/CLUS_CSV_VOLUME_NAME, clusapi/PCLUS_CSV_VOLUME_NAME, mscs.clus_csv_volume_name'
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2 Datacenter, Windows Server 2008 R2 Enterprise
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
req.typenames: CLUS_CSV_VOLUME_NAME, *PCLUS_CSV_VOLUME_NAME
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CLUS_CSV_VOLUME_NAME
 - clusapi/_CLUS_CSV_VOLUME_NAME
 - PCLUS_CSV_VOLUME_NAME
 - clusapi/PCLUS_CSV_VOLUME_NAME
 - CLUS_CSV_VOLUME_NAME
 - clusapi/CLUS_CSV_VOLUME_NAME
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
 - CLUS_CSV_VOLUME_NAME
---

# CLUS_CSV_VOLUME_NAME structure


## -description

Represents the name of a cluster shared volume (CSV).

## -struct-fields

### -field VolumeOffset

The physical offset, in bytes, of the data on the CSV.

### -field szVolumeName

A Unicode string that contains the volume name of the CSV. The string has a terminating null character.  The name provided can be either the cluster-assigned friendly name or the volume <b>GUID</b> path of the form "\\?\Volume{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}\".

### -field szRootPath

The root path of the CSV.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/data-structures">Data structures</a>