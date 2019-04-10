---
UID: NS:clusapi.CLUSPROP_SCSI_ADDRESS
title: CLUSPROP_SCSI_ADDRESS (clusapi.h)
author: windows-sdk-content
description: Describes an address for a SCSI device.
old-location: mscs\clusprop_scsi_address.htm
tech.root: MsCS
ms.assetid: 30907886-0c86-4e8a-9a95-5b62f6ffff76
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PCLUSPROP_SCSI_ADDRESS, CLUSPROP_SCSI_ADDRESS, CLUSPROP_SCSI_ADDRESS structure [Failover Cluster], PCLUSPROP_SCSI_ADDRESS, PCLUSPROP_SCSI_ADDRESS structure pointer [Failover Cluster], _wolf_clusprop_scsi_address, clusapi/CLUSPROP_SCSI_ADDRESS, clusapi/PCLUSPROP_SCSI_ADDRESS, mscs.clusprop_scsi_address"
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
 - CLUSPROP_SCSI_ADDRESS
product: Windows
targetos: Windows
req.typenames: CLUSPROP_SCSI_ADDRESS, *PCLUSPROP_SCSI_ADDRESS
req.redist: 
---

# CLUSPROP_SCSI_ADDRESS structure


## -description


Describes an address for a <a href="https://msdn.microsoft.com/en-us/library/Aa372937(v=VS.85).aspx">SCSI</a> 
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


<a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> structure with a <a href="https://msdn.microsoft.com/23353e11-63bb-4d3b-90fb-e2a5544e0d09">CLUSPROP_SYNTAX</a>  with a value 
       of <b>CLUSPROP_SYNTAX_SCSI_ADDRESS</b> (0x00060002) and a <b>cbLength</b> field indicating 
       the count of bytes in the <b>CLUS_SCSI_ADDRESS</b> member. Padding bytes are not included in the count.


### -field CLUS_SCSI_ADDRESS

A <a href="https://msdn.microsoft.com/05a640c7-16b4-4394-b22f-a78ab1dfab77">CLUS_SCSI_ADDRESS</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/23353e11-63bb-4d3b-90fb-e2a5544e0d09">CLUSPROP_SYNTAX</a>



<a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a>



<a href="https://msdn.microsoft.com/b8b6c479-2e35-4cc9-b864-d495c3bded25">CLUS_SCSI_ADDRESS</a>



<a href="https://msdn.microsoft.com/7becbcf6-bad9-44e2-9731-d53de8299b99">ClusScsiAddress</a>



<a href="https://msdn.microsoft.com/e3ad7c34-0c8a-4f03-8e5c-b57802c493f0">Data structures</a>
 

 

