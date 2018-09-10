---
UID: NS:clusapi.CLUS_MAINTENANCE_MODE_INFO
title: CLUS_MAINTENANCE_MODE_INFO
author: windows-sdk-content
description: Enables or disables maintenance mode on a cluster node.
old-location: mscs\clus_maintenance_mode_info.htm
tech.root: mscs
ms.assetid: dc53dc5e-b7ed-49f8-a08f-495e2c0e45e2
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PCLUS_MAINTENANCE_MODE_INFO, CLUS_MAINTENANCE_MODE_INFO, CLUS_MAINTENANCE_MODE_INFO structure [Failover Cluster], PCLUS_MAINTENANCE_MODE_INFO, PCLUS_MAINTENANCE_MODE_INFO structure pointer [Failover Cluster], clusapi/CLUS_MAINTENANCE_MODE_INFO, clusapi/PCLUS_MAINTENANCE_MODE_INFO, mscs.clus_maintenance_mode_info"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise with SP1, Windows Server 2008 Datacenter with SP1
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
 - CLUS_MAINTENANCE_MODE_INFO
product: Windows
targetos: Windows
req.typenames: CLUS_MAINTENANCE_MODE_INFO, *PCLUS_MAINTENANCE_MODE_INFO
req.redist: 
---

# CLUS_MAINTENANCE_MODE_INFO structure


## -description


Enables or disables maintenance mode on a cluster node.


## -struct-fields




### -field InMaintenance

Set to <b>TRUE</b> to enable or <b>FALSE</b> to disable maintenance 
      mode for the identified resource.

When queried, a resource will return <b>True</b> or <b>False</b> to 
       indicate the current maintenance mode state of the resource.


## -remarks



When using <a href="https://msdn.microsoft.com/en-us/library/Aa369016(v=VS.85).aspx">ClusterResourceControl</a> to enable 
    or disable maintenance mode on a specified resource, the calling routine can specify a larger buffer with addition 
    resource-specific data by including it immediately after the 
    <b>CLUS_MAINTENANCE_MODE_INFO</b> structure. This 
    data then becomes private to the resource as it cannot be retrieved by the calling program using the 
    <a href="https://msdn.microsoft.com/en-us/library/Aa367486(v=VS.85).aspx">CLUSCTL_RESOURCE_QUERY_MAINTENANCE_MODE</a> 
    control code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa367486(v=VS.85).aspx">CLUSCTL_RESOURCE_QUERY_MAINTENANCE_MODE</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa367490(v=VS.85).aspx">CLUSCTL_RESOURCE_SET_MAINTENANCE_MODE</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa369016(v=VS.85).aspx">ClusterResourceControl</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa373109(v=VS.85).aspx">Utility structures</a>
 

 

