---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# CLUS_SCSI_ADDRESS structure


## -description


Contains <a href="s_gly.htm">SCSI</a> address data. It is 
    used as the data member of a <a href="https://msdn.microsoft.com/30907886-0c86-4e8a-9a95-5b62f6ffff76">CLUSPROP_SCSI_ADDRESS</a> 
    structure and as the return value of some <a href="https://msdn.microsoft.com/47618915-0985-4415-b7d4-5959fb27eb9f">control code</a> 
    operations.


## -struct-fields




### -field DUMMYUNIONNAME


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.PortNumber

Identifies the SCSI controller. This corresponds to the 
         <a href="https://msdn.microsoft.com/a05715d8-4eae-4a80-bba3-9b26e90ba6d4">PortNumber</a> property of the 
         <a href="https://msdn.microsoft.com/7becbcf6-bad9-44e2-9731-d53de8299b99">ClusScsiAddress</a> object.


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.PathId

Identifies the bus on the SCSI controller specified by <b>PortNumber</b>. This 
         corresponds to the <a href="https://msdn.microsoft.com/c46946bb-87a8-4444-92c7-d15720a7fdd5">PathId</a> property of the 
         <a href="https://msdn.microsoft.com/7becbcf6-bad9-44e2-9731-d53de8299b99">ClusScsiAddress</a> object.


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.TargetId

Identifies the target device on the SCSI bus specified by <b>PathId</b>. This 
         corresponds to the <a href="https://msdn.microsoft.com/878c9914-2706-4aaf-9b44-2c2a7ca2e067">TargetId</a> property of 
         the <a href="https://msdn.microsoft.com/7becbcf6-bad9-44e2-9731-d53de8299b99">ClusScsiAddress</a> object.


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.Lun

Identifies the individual logical unit at the target device specified by 
         <b>TargetId</b>. This corresponds to the 
         <a href="https://msdn.microsoft.com/47ac3714-fe5c-4b3b-9271-57980981785d">Lun</a> property of the 
         <a href="https://msdn.microsoft.com/7becbcf6-bad9-44e2-9731-d53de8299b99">ClusScsiAddress</a> object.


### -field DUMMYUNIONNAME.dw

Numeric value that describes the SCSI address as a combination of the <b>PortNumber</b>, 
        <b>PathId</b>, <b>TargetId</b>, and <b>Lun</b> 
        values.


## -remarks



A <b>CLUS_SCSI_ADDRESS</b> structure can also be returned 
     by <a href="https://msdn.microsoft.com/a98ca55a-6535-48cf-a925-5005baa01b94">ClusterResourceControl</a> when the 
     <i>dwControlCode</i> parameter is set to 
     <a href="https://msdn.microsoft.com/e80dfab7-448a-4d68-aae8-c6b42c5dc6f9">CLUSCTL_RESOURCE_STORAGE_GET_DISK_INFO</a> 
     and can be returned by 
     <a href="https://msdn.microsoft.com/79f4949d-e5ef-4d2e-ac11-0e30b6c566fd">ClusterResourceTypeControl</a> when 
     <i>dwControlCode</i> is set to 
     <a href="https://msdn.microsoft.com/2df1eeb4-ecad-4065-866c-545476a43d9b">CLUSCTL_RESOURCE_TYPE_STORAGE_GET_AVAILABLE_DISKS</a>.


#### Examples

See 
      <a href="https://msdn.microsoft.com/003bc879-d526-4f7d-8f58-a9002f78819d">Creating Physical Disk Resources</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/e80dfab7-448a-4d68-aae8-c6b42c5dc6f9">CLUSCTL_RESOURCE_STORAGE_GET_DISK_INFO</a>



<a href="https://msdn.microsoft.com/2df1eeb4-ecad-4065-866c-545476a43d9b">CLUSCTL_RESOURCE_TYPE_STORAGE_GET_AVAILABLE_DISKS</a>



<a href="https://msdn.microsoft.com/30907886-0c86-4e8a-9a95-5b62f6ffff76">CLUSPROP_SCSI_ADDRESS</a>



<a href="https://msdn.microsoft.com/7becbcf6-bad9-44e2-9731-d53de8299b99">ClusScsiAddress Object</a>



<a href="https://msdn.microsoft.com/a98ca55a-6535-48cf-a925-5005baa01b94">ClusterResourceControl</a>



<a href="https://msdn.microsoft.com/79f4949d-e5ef-4d2e-ac11-0e30b6c566fd">ClusterResourceTypeControl</a>
 

 

