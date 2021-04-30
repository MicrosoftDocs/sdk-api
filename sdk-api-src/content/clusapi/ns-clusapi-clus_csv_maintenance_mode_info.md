---
UID: NS:clusapi.CLUS_CSV_MAINTENANCE_MODE_INFO
title: CLUS_CSV_MAINTENANCE_MODE_INFO (clusapi.h)
description: Enables or disables the maintenance mode on a cluster shared volume (CSV).
helpviewer_keywords: ["*PCLUS_CSV_MAINTENANCE_MODE_INFO","CLUS_CSV_MAINTENANCE_MODE_INFO","CLUS_CSV_MAINTENANCE_MODE_INFO structure [Failover Cluster]","PCLUS_CSV_MAINTENANCE_MODE_INFO","PCLUS_CSV_MAINTENANCE_MODE_INFO structure pointer [Failover Cluster]","clusapi/CLUS_CSV_MAINTENANCE_MODE_INFO","clusapi/PCLUS_CSV_MAINTENANCE_MODE_INFO","mscs.clus_csv_maintenance_mode_info"]
old-location: mscs\clus_csv_maintenance_mode_info.htm
tech.root: MsCS
ms.assetid: 4DA05ADE-3C54-45A0-8A1C-911EB1ED1308
ms.date: 12/05/2018
ms.keywords: '*PCLUS_CSV_MAINTENANCE_MODE_INFO, CLUS_CSV_MAINTENANCE_MODE_INFO, CLUS_CSV_MAINTENANCE_MODE_INFO structure [Failover Cluster], PCLUS_CSV_MAINTENANCE_MODE_INFO, PCLUS_CSV_MAINTENANCE_MODE_INFO structure pointer [Failover Cluster], clusapi/CLUS_CSV_MAINTENANCE_MODE_INFO, clusapi/PCLUS_CSV_MAINTENANCE_MODE_INFO, mscs.clus_csv_maintenance_mode_info'
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
req.typenames: CLUS_CSV_MAINTENANCE_MODE_INFO, *PCLUS_CSV_MAINTENANCE_MODE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUS_CSV_MAINTENANCE_MODE_INFO
 - clusapi/CLUS_CSV_MAINTENANCE_MODE_INFO
 - PCLUS_CSV_MAINTENANCE_MODE_INFO
 - clusapi/PCLUS_CSV_MAINTENANCE_MODE_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusApi.h
api_name:
 - CLUS_CSV_MAINTENANCE_MODE_INFO
---

# CLUS_CSV_MAINTENANCE_MODE_INFO structure


## -description

Used with the 
    <a href="/previous-versions/windows/desktop/mscs/clusctl-resource-set-csv-maintenance-mode">CLUSCTL_RESOURCE_SET_CSV_MAINTENANCE_MODE</a> 
    control code to enables or disables the  maintenance mode on a cluster shared volume (CSV).

## -struct-fields

### -field InMaintenance

Specifies the maintenance mode for the CSV. <b>TRUE</b> enables maintenance mode, 
      <b>FALSE</b> disables it.

### -field VolumeName

The volume <b>GUID</b> path of the CSV.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-set-csv-maintenance-mode">CLUSCTL_RESOURCE_SET_CSV_MAINTENANCE_MODE</a>



<a href="/previous-versions/windows/desktop/mscs/utility-structures">Utility structures</a>