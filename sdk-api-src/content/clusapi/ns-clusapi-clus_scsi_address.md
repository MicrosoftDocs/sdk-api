---
UID: NS:clusapi.CLUS_SCSI_ADDRESS
title: CLUS_SCSI_ADDRESS (clusapi.h)
description: Contains SCSI address data. It is used as the data member of a CLUSPROP_SCSI_ADDRESS structure and as the return value of some control code operations.
helpviewer_keywords: ["*PCLUS_SCSI_ADDRESS","CLUS_SCSI_ADDRESS","CLUS_SCSI_ADDRESS structure [Failover Cluster]","PCLUS_SCSI_ADDRESS","PCLUS_SCSI_ADDRESS structure pointer [Failover Cluster]","_wolf_clus_scsi_address","clusapi/CLUS_SCSI_ADDRESS","clusapi/PCLUS_SCSI_ADDRESS","mscs.clus_scsi_address"]
old-location: mscs\clus_scsi_address.htm
tech.root: MsCS
ms.assetid: 05a640c7-16b4-4394-b22f-a78ab1dfab77
ms.date: 12/05/2018
ms.keywords: '*PCLUS_SCSI_ADDRESS, CLUS_SCSI_ADDRESS, CLUS_SCSI_ADDRESS structure [Failover Cluster], PCLUS_SCSI_ADDRESS, PCLUS_SCSI_ADDRESS structure pointer [Failover Cluster], _wolf_clus_scsi_address, clusapi/CLUS_SCSI_ADDRESS, clusapi/PCLUS_SCSI_ADDRESS, mscs.clus_scsi_address'
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
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
req.typenames: CLUS_SCSI_ADDRESS, *PCLUS_SCSI_ADDRESS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUS_SCSI_ADDRESS
 - clusapi/CLUS_SCSI_ADDRESS
 - PCLUS_SCSI_ADDRESS
 - clusapi/PCLUS_SCSI_ADDRESS
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
 - CLUS_SCSI_ADDRESS
---

# CLUS_SCSI_ADDRESS structure


## -description

Contains <a href="/previous-versions/windows/desktop/mscs/s-gly">SCSI</a> address data. It is 
    used as the data member of a <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_scsi_address">CLUSPROP_SCSI_ADDRESS</a> 
    structure and as the return value of some <a href="/previous-versions/windows/desktop/mscs/control-codes">control code</a> 
    operations.

## -struct-fields

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.PortNumber

Identifies the SCSI controller. This corresponds to the 
         <a href="/previous-versions/windows/desktop/mscs/clusscsiaddress-portnumber">PortNumber</a> property of the 
         <a href="/previous-versions/windows/desktop/mscs/clusscsiaddress-object">ClusScsiAddress</a> object.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.PathId

Identifies the bus on the SCSI controller specified by <b>PortNumber</b>. This 
         corresponds to the <a href="/previous-versions/windows/desktop/mscs/clusscsiaddress-pathid">PathId</a> property of the 
         <a href="/previous-versions/windows/desktop/mscs/clusscsiaddress-object">ClusScsiAddress</a> object.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.TargetId

Identifies the target device on the SCSI bus specified by <b>PathId</b>. This 
         corresponds to the <a href="/previous-versions/windows/desktop/mscs/clusscsiaddress-targetid">TargetId</a> property of 
         the <a href="/previous-versions/windows/desktop/mscs/clusscsiaddress-object">ClusScsiAddress</a> object.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.Lun

Identifies the individual logical unit at the target device specified by 
         <b>TargetId</b>. This corresponds to the 
         <a href="/previous-versions/windows/desktop/mscs/clusscsiaddress-lun">Lun</a> property of the 
         <a href="/previous-versions/windows/desktop/mscs/clusscsiaddress-object">ClusScsiAddress</a> object.

### -field DUMMYUNIONNAME.dw

Numeric value that describes the SCSI address as a combination of the <b>PortNumber</b>, 
        <b>PathId</b>, <b>TargetId</b>, and <b>Lun</b> 
        values.

## -remarks

A <b>CLUS_SCSI_ADDRESS</b> structure can also be returned 
     by <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterresourcecontrol">ClusterResourceControl</a> when the 
     <i>dwControlCode</i> parameter is set to 
     <a href="/previous-versions/windows/desktop/mscs/clusctl-resource-storage-get-disk-info">CLUSCTL_RESOURCE_STORAGE_GET_DISK_INFO</a> 
     and can be returned by 
     <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterresourcetypecontrol">ClusterResourceTypeControl</a> when 
     <i>dwControlCode</i> is set to 
     <a href="/previous-versions/windows/desktop/mscs/clusctl-resource-type-storage-get-available-disks">CLUSCTL_RESOURCE_TYPE_STORAGE_GET_AVAILABLE_DISKS</a>.


#### Examples

See 
      <a href="/previous-versions/windows/desktop/mscs/creating-physical-disk-resources">Creating Physical Disk Resources</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-storage-get-disk-info">CLUSCTL_RESOURCE_STORAGE_GET_DISK_INFO</a>



<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-type-storage-get-available-disks">CLUSCTL_RESOURCE_TYPE_STORAGE_GET_AVAILABLE_DISKS</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_scsi_address">CLUSPROP_SCSI_ADDRESS</a>



<a href="/previous-versions/windows/desktop/mscs/clusscsiaddress-object">ClusScsiAddress Object</a>



<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterresourcecontrol">ClusterResourceControl</a>



<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterresourcetypecontrol">ClusterResourceTypeControl</a>