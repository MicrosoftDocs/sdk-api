---
UID: NS:clusapi.CLUSPROP_SCSI_ADDRESS
title: CLUSPROP_SCSI_ADDRESS
author: windows-sdk-content
description: Describes an address for a SCSI device.
old-location: mscs\clusprop_scsi_address.htm
old-project: mscs
ms.assetid: 30907886-0c86-4e8a-9a95-5b62f6ffff76
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: "*PCLUSPROP_SCSI_ADDRESS, CLUSPROP_SCSI_ADDRESS, CLUSPROP_SCSI_ADDRESS structure [Failover Cluster], PCLUSPROP_SCSI_ADDRESS, PCLUSPROP_SCSI_ADDRESS structure pointer [Failover Cluster], _wolf_clusprop_scsi_address, clusapi/CLUSPROP_SCSI_ADDRESS, clusapi/PCLUSPROP_SCSI_ADDRESS, mscs.clusprop_scsi_address"
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
tech.root: 
req.typenames: CLUSPROP_SCSI_ADDRESS, *PCLUSPROP_SCSI_ADDRESS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
api_name:
 - CLUSPROP_SCSI_ADDRESS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# CLUSPROP_SCSI_ADDRESS structure


## -description


Describes an address for a <a href="s_gly.htm">SCSI</a> 
    device. It is used as an entry in a <a href="https://msdn.microsoft.com/f2b20fe5-0d7e-4ccd-b288-aa8104a24fef">value list</a> and consists 
    of:
<ul>
<li>A <a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> structure indicating the format 
     and type of the resource class information.</li>
<li>A <a href="https://msdn.microsoft.com/05a640c7-16b4-4394-b22f-a78ab1dfab77">CLUS_SCSI_ADDRESS</a> structure.</li>
</ul>For convenience, the <a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> and 
    <a href="https://msdn.microsoft.com/05a640c7-16b4-4394-b22f-a78ab1dfab77">CLUS_SCSI_ADDRESS</a> members are listed explicitly.


## -struct-fields




### -field CLUSPROP_VALUE

 


### -field CLUS_SCSI_ADDRESS

 




#### - Lun

Member of the <a href="https://msdn.microsoft.com/05a640c7-16b4-4394-b22f-a78ab1dfab77">CLUS_SCSI_ADDRESS</a> structure that 
         identifies the individual logical unit number (LUN) at the target device specified by the 
         <b>TargetId</b> member. This corresponds to the 
         <a href="https://msdn.microsoft.com/47ac3714-fe5c-4b3b-9271-57980981785d">Lun</a> property of the 
         <a href="https://msdn.microsoft.com/7becbcf6-bad9-44e2-9731-d53de8299b99">ClusScsiAddress</a> object.


#### - PathId

Member of the <a href="https://msdn.microsoft.com/05a640c7-16b4-4394-b22f-a78ab1dfab77">CLUS_SCSI_ADDRESS</a> structure that 
         identifies the bus on the SCSI controller specified by <b>PortNumber</b>. This 
         corresponds to the <a href="https://msdn.microsoft.com/c46946bb-87a8-4444-92c7-d15720a7fdd5">PathId</a> property of the 
         <a href="https://msdn.microsoft.com/7becbcf6-bad9-44e2-9731-d53de8299b99">ClusScsiAddress</a> object.


#### - PortNumber

Member of the <a href="https://msdn.microsoft.com/05a640c7-16b4-4394-b22f-a78ab1dfab77">CLUS_SCSI_ADDRESS</a> structure that 
         identifies port number of the SCSI controller. This corresponds to the 
         <a href="https://msdn.microsoft.com/a05715d8-4eae-4a80-bba3-9b26e90ba6d4">PortNumber</a> property of the 
         <a href="https://msdn.microsoft.com/7becbcf6-bad9-44e2-9731-d53de8299b99">ClusScsiAddress</a> object.


#### - Syntax

Member of the <a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> structure with a value 
       of <b>CLUSPROP_SYNTAX_SCSI_ADDRESS</b> (0x00060002).


#### - TargetId

Member of the <a href="https://msdn.microsoft.com/05a640c7-16b4-4394-b22f-a78ab1dfab77">CLUS_SCSI_ADDRESS</a> structure that 
         identifies the target device on SCSI bus specified by <b>PathId</b>. This corresponds to 
         the <a href="https://msdn.microsoft.com/878c9914-2706-4aaf-9b44-2c2a7ca2e067">TargetId</a> property of the 
         <a href="https://msdn.microsoft.com/7becbcf6-bad9-44e2-9731-d53de8299b99">ClusScsiAddress</a> object.


#### - cbLength

Member of the <a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> structure indicating 
       the count of bytes in the <a href="https://msdn.microsoft.com/05a640c7-16b4-4394-b22f-a78ab1dfab77">CLUS_SCSI_ADDRESS</a> 
       structure that follows the <b>CLUSPROP_VALUE</b> header. 
       Padding bytes are not included in the count.


#### - dw

Member of the <a href="https://msdn.microsoft.com/05a640c7-16b4-4394-b22f-a78ab1dfab77">CLUS_SCSI_ADDRESS</a> structure that 
        describes the SCSI address as a combination of the <b>PortNumber</b>, 
        <b>PathId</b>, <b>TargetId</b>, and <b>Lun</b> 
        values.


## -see-also




<a href="https://msdn.microsoft.com/23353e11-63bb-4d3b-90fb-e2a5544e0d09">CLUSPROP_SYNTAX</a>



<a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a>



<a href="https://msdn.microsoft.com/b8b6c479-2e35-4cc9-b864-d495c3bded25">CLUS_SCSI_ADDRESS</a>



<a href="https://msdn.microsoft.com/7becbcf6-bad9-44e2-9731-d53de8299b99">ClusScsiAddress</a>



<a href="https://msdn.microsoft.com/e3ad7c34-0c8a-4f03-8e5c-b57802c493f0">Data structures</a>
 

 

