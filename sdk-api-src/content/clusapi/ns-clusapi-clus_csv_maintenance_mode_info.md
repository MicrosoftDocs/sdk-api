---
UID: NS:clusapi.CLUS_CSV_MAINTENANCE_MODE_INFO
title: CLUS_CSV_MAINTENANCE_MODE_INFO
author: windows-sdk-content
description: Enables or disables the maintenance mode on a cluster shared volume (CSV).
old-location: mscs\clus_csv_maintenance_mode_info.htm
tech.root: MsCS
ms.assetid: 4DA05ADE-3C54-45A0-8A1C-911EB1ED1308
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PCLUS_CSV_MAINTENANCE_MODE_INFO, CLUS_CSV_MAINTENANCE_MODE_INFO, CLUS_CSV_MAINTENANCE_MODE_INFO structure [Failover Cluster], PCLUS_CSV_MAINTENANCE_MODE_INFO, PCLUS_CSV_MAINTENANCE_MODE_INFO structure pointer [Failover Cluster], clusapi/CLUS_CSV_MAINTENANCE_MODE_INFO, clusapi/PCLUS_CSV_MAINTENANCE_MODE_INFO, mscs.clus_csv_maintenance_mode_info"
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
 - ClusApi.h
api_name:
 - CLUS_CSV_MAINTENANCE_MODE_INFO
product: Windows
targetos: Windows
req.typenames: CLUS_CSV_MAINTENANCE_MODE_INFO, *PCLUS_CSV_MAINTENANCE_MODE_INFO
req.redist: 
---

# CLUS_CSV_MAINTENANCE_MODE_INFO structure


## -description


Used with the 
    <a href="https://msdn.microsoft.com/12c35048-660d-47d3-b35c-24eea5627ffb">CLUSCTL_RESOURCE_SET_CSV_MAINTENANCE_MODE</a> 
    control code to enables or disables the  maintenance mode on a cluster shared volume (CSV).


## -struct-fields




### -field InMaintenance

Specifies the maintenance mode for the CSV. <b>TRUE</b> enables maintenance mode, 
      <b>FALSE</b> disables it.


### -field VolumeName

The volume <b>GUID</b> path of the CSV.


## -see-also




<a href="https://msdn.microsoft.com/12c35048-660d-47d3-b35c-24eea5627ffb">CLUSCTL_RESOURCE_SET_CSV_MAINTENANCE_MODE</a>



<a href="https://msdn.microsoft.com/45da8dbc-dd70-4f95-b933-66d8e4340448">Utility structures</a>
 

 

