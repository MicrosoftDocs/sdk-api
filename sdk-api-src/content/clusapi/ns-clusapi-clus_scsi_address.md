---
UID: NS:clusapi.CLUS_SCSI_ADDRESS
title: CLUS_SCSI_ADDRESS
author: windows-sdk-content
description: Contains SCSI address data. It is used as the data member of a CLUSPROP_SCSI_ADDRESS structure and as the return value of some control code operations.
old-location: mscs\clus_scsi_address.htm
tech.root: mscs
ms.assetid: 05a640c7-16b4-4394-b22f-a78ab1dfab77
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: "*PCLUS_SCSI_ADDRESS, CLUS_SCSI_ADDRESS, CLUS_SCSI_ADDRESS structure [Failover Cluster], PCLUS_SCSI_ADDRESS, PCLUS_SCSI_ADDRESS structure pointer [Failover Cluster], _wolf_clus_scsi_address, clusapi/CLUS_SCSI_ADDRESS, clusapi/PCLUS_SCSI_ADDRESS, mscs.clus_scsi_address"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
api_name:
 - CLUS_SCSI_ADDRESS
product: Windows
targetos: Windows
req.typenames: CLUS_SCSI_ADDRESS, *PCLUS_SCSI_ADDRESS
req.redist: 
---

# CLUS_SCSI_ADDRESS structure


## -description


Contains <a href="https://msdn.microsoft.com/en-us/library/Aa372937(v=VS.85).aspx">SCSI</a> address data. It is 
    used as the data member of a <a href="https://msdn.microsoft.com/en-us/library/Aa368387(v=VS.85).aspx">CLUSPROP_SCSI_ADDRESS</a> 
    structure and as the return value of some <a href="https://msdn.microsoft.com/47618915-0985-4415-b7d4-5959fb27eb9f">control code</a> 
    operations.


## -struct-fields




### -field DUMMYUNIONNAME


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.PortNumber

Identifies the SCSI controller. This corresponds to the 
         <a href="https://msdn.microsoft.com/en-us/library/Aa368830(v=VS.85).aspx">PortNumber</a> property of the 
         <a href="https://msdn.microsoft.com/en-us/library/Aa368828(v=VS.85).aspx">ClusScsiAddress</a> object.


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.PathId

Identifies the bus on the SCSI controller specified by <b>PortNumber</b>. This 
         corresponds to the <a href="https://msdn.microsoft.com/en-us/library/Aa368829(v=VS.85).aspx">PathId</a> property of the 
         <a href="https://msdn.microsoft.com/en-us/library/Aa368828(v=VS.85).aspx">ClusScsiAddress</a> object.


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.TargetId

Identifies the target device on the SCSI bus specified by <b>PathId</b>. This 
         corresponds to the <a href="https://msdn.microsoft.com/en-us/library/Aa368831(v=VS.85).aspx">TargetId</a> property of 
         the <a href="https://msdn.microsoft.com/en-us/library/Aa368828(v=VS.85).aspx">ClusScsiAddress</a> object.


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.Lun

Identifies the individual logical unit at the target device specified by 
         <b>TargetId</b>. This corresponds to the 
         <a href="https://msdn.microsoft.com/en-us/library/Aa368827(v=VS.85).aspx">Lun</a> property of the 
         <a href="https://msdn.microsoft.com/en-us/library/Aa368828(v=VS.85).aspx">ClusScsiAddress</a> object.


### -field DUMMYUNIONNAME.dw

Numeric value that describes the SCSI address as a combination of the <b>PortNumber</b>, 
        <b>PathId</b>, <b>TargetId</b>, and <b>Lun</b> 
        values.


## -remarks



A <b>CLUS_SCSI_ADDRESS</b> structure can also be returned 
     by <a href="https://msdn.microsoft.com/en-us/library/Aa369016(v=VS.85).aspx">ClusterResourceControl</a> when the 
     <i>dwControlCode</i> parameter is set to 
     <a href="https://msdn.microsoft.com/en-us/library/Aa367495(v=VS.85).aspx">CLUSCTL_RESOURCE_STORAGE_GET_DISK_INFO</a> 
     and can be returned by 
     <a href="https://msdn.microsoft.com/en-us/library/Aa369036(v=VS.85).aspx">ClusterResourceTypeControl</a> when 
     <i>dwControlCode</i> is set to 
     <a href="https://msdn.microsoft.com/en-us/library/Aa367675(v=VS.85).aspx">CLUSCTL_RESOURCE_TYPE_STORAGE_GET_AVAILABLE_DISKS</a>.


#### Examples

See 
      <a href="https://msdn.microsoft.com/en-us/library/Aa369328(v=VS.85).aspx">Creating Physical Disk Resources</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa367495(v=VS.85).aspx">CLUSCTL_RESOURCE_STORAGE_GET_DISK_INFO</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa367675(v=VS.85).aspx">CLUSCTL_RESOURCE_TYPE_STORAGE_GET_AVAILABLE_DISKS</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa368387(v=VS.85).aspx">CLUSPROP_SCSI_ADDRESS</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa368828(v=VS.85).aspx">ClusScsiAddress Object</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa369016(v=VS.85).aspx">ClusterResourceControl</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa369036(v=VS.85).aspx">ClusterResourceTypeControl</a>
 

 

