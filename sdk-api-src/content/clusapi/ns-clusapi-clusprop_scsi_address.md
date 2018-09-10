---
UID: NS:clusapi.CLUSPROP_SCSI_ADDRESS
title: CLUSPROP_SCSI_ADDRESS
author: windows-sdk-content
description: Describes an address for a SCSI device.
old-location: mscs\clusprop_scsi_address.htm
tech.root: mscs
ms.assetid: 30907886-0c86-4e8a-9a95-5b62f6ffff76
ms.author: windowssdkdev
ms.date: 08/29/2018
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
    device. It is used as an entry in a <a href="https://msdn.microsoft.com/en-us/library/Aa373112(v=VS.85).aspx">value list</a> and consists 
    of:
<ul>
<li>A <a href="https://msdn.microsoft.com/en-us/library/Aa368393(v=VS.85).aspx">CLUSPROP_VALUE</a> structure indicating the format 
     and type of the resource class information.</li>
<li>A <a href="https://msdn.microsoft.com/en-us/library/Aa369188(v=VS.85).aspx">CLUS_SCSI_ADDRESS</a> structure.</li>
</ul>For convenience, the <a href="https://msdn.microsoft.com/en-us/library/Aa368393(v=VS.85).aspx">CLUSPROP_VALUE</a> and 
    <a href="https://msdn.microsoft.com/en-us/library/Aa369188(v=VS.85).aspx">CLUS_SCSI_ADDRESS</a> members are listed explicitly.


## -struct-fields




### -field CLUSPROP_VALUE

 


### -field CLUS_SCSI_ADDRESS

 




#### - Lun

Member of the <a href="https://msdn.microsoft.com/en-us/library/Aa369188(v=VS.85).aspx">CLUS_SCSI_ADDRESS</a> structure that 
         identifies the individual logical unit number (LUN) at the target device specified by the 
         <b>TargetId</b> member. This corresponds to the 
         <a href="https://msdn.microsoft.com/en-us/library/Aa368827(v=VS.85).aspx">Lun</a> property of the 
         <a href="https://msdn.microsoft.com/en-us/library/Aa368828(v=VS.85).aspx">ClusScsiAddress</a> object.


#### - PathId

Member of the <a href="https://msdn.microsoft.com/en-us/library/Aa369188(v=VS.85).aspx">CLUS_SCSI_ADDRESS</a> structure that 
         identifies the bus on the SCSI controller specified by <b>PortNumber</b>. This 
         corresponds to the <a href="https://msdn.microsoft.com/en-us/library/Aa368829(v=VS.85).aspx">PathId</a> property of the 
         <a href="https://msdn.microsoft.com/en-us/library/Aa368828(v=VS.85).aspx">ClusScsiAddress</a> object.


#### - PortNumber

Member of the <a href="https://msdn.microsoft.com/en-us/library/Aa369188(v=VS.85).aspx">CLUS_SCSI_ADDRESS</a> structure that 
         identifies port number of the SCSI controller. This corresponds to the 
         <a href="https://msdn.microsoft.com/en-us/library/Aa368830(v=VS.85).aspx">PortNumber</a> property of the 
         <a href="https://msdn.microsoft.com/en-us/library/Aa368828(v=VS.85).aspx">ClusScsiAddress</a> object.


#### - Syntax

Member of the <a href="https://msdn.microsoft.com/en-us/library/Aa368393(v=VS.85).aspx">CLUSPROP_VALUE</a> structure with a value 
       of <b>CLUSPROP_SYNTAX_SCSI_ADDRESS</b> (0x00060002).


#### - TargetId

Member of the <a href="https://msdn.microsoft.com/en-us/library/Aa369188(v=VS.85).aspx">CLUS_SCSI_ADDRESS</a> structure that 
         identifies the target device on SCSI bus specified by <b>PathId</b>. This corresponds to 
         the <a href="https://msdn.microsoft.com/en-us/library/Aa368831(v=VS.85).aspx">TargetId</a> property of the 
         <a href="https://msdn.microsoft.com/en-us/library/Aa368828(v=VS.85).aspx">ClusScsiAddress</a> object.


#### - cbLength

Member of the <a href="https://msdn.microsoft.com/en-us/library/Aa368393(v=VS.85).aspx">CLUSPROP_VALUE</a> structure indicating 
       the count of bytes in the <a href="https://msdn.microsoft.com/en-us/library/Aa369188(v=VS.85).aspx">CLUS_SCSI_ADDRESS</a> 
       structure that follows the <b>CLUSPROP_VALUE</b> header. 
       Padding bytes are not included in the count.


#### - dw

Member of the <a href="https://msdn.microsoft.com/en-us/library/Aa369188(v=VS.85).aspx">CLUS_SCSI_ADDRESS</a> structure that 
        describes the SCSI address as a combination of the <b>PortNumber</b>, 
        <b>PathId</b>, <b>TargetId</b>, and <b>Lun</b> 
        values.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa368389(v=VS.85).aspx">CLUSPROP_SYNTAX</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa368393(v=VS.85).aspx">CLUSPROP_VALUE</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa369187(v=VS.85).aspx">CLUS_SCSI_ADDRESS</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa368828(v=VS.85).aspx">ClusScsiAddress</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa369339(v=VS.85).aspx">Data structures</a>
 

 

