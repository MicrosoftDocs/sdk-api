---
UID: NS:clusapi.CLUSPROP_PARTITION_INFO
title: CLUSPROP_PARTITION_INFO (clusapi.h)
author: windows-sdk-content
description: Contains information relevant to storage class resources.
old-location: mscs\clusprop_partition_info.htm
tech.root: MsCS
ms.assetid: cda1e334-dba8-4fe9-b035-4e475245869c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PCLUSPROP_PARTITION_INFO, CLUSPROP_PARTITION_INFO, CLUSPROP_PARTITION_INFO structure [Failover Cluster], PCLUSPROP_PARTITION_INFO, PCLUSPROP_PARTITION_INFO structure pointer [Failover Cluster], _wolf_clusprop_partition_info, clusapi/CLUSPROP_PARTITION_INFO, clusapi/PCLUSPROP_PARTITION_INFO, mscs.clusprop_partition_info"
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
 - CLUSPROP_PARTITION_INFO
product: Windows
targetos: Windows
req.typenames: CLUSPROP_PARTITION_INFO, *PCLUSPROP_PARTITION_INFO
req.redist: 
---

# CLUSPROP_PARTITION_INFO structure


## -description


Contains 
    information relevant to 
    <a href="https://msdn.microsoft.com/en-us/library/Aa372937(v=VS.85).aspx">storage class resources</a>. It is used as an 
    entry in a <a href="https://msdn.microsoft.com/f2b20fe5-0d7e-4ccd-b288-aa8104a24fef">value list</a> and consists of:
<ul>
<li>A <a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> structure describing the format, 
     type, and length of the partition information.</li>
<li>A <a href="https://msdn.microsoft.com/656b230d-b4ba-45e4-b6b3-8bbe72f9428a">CLUS_PARTITION_INFO</a> structure.</li>
</ul>For convenience, the <a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> and 
    <a href="https://msdn.microsoft.com/656b230d-b4ba-45e4-b6b3-8bbe72f9428a">CLUS_PARTITION_INFO</a> members are listed 
    explicitly.


## -struct-fields




### -field CLUSPROP_VALUE


<a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> structure with a <a href="https://msdn.microsoft.com/23353e11-63bb-4d3b-90fb-e2a5544e0d09">CLUSPROP_SYNTAX</a>  with a value 
       of <b>CLUSPROP_SYNTAX_PARTITION_INFO</b> (0x00080001) and a <b>cbLength</b> field indicating 
       the count of bytes in the <b>CLUS_PARTITION_INFO</b> member.


### -field CLUS_PARTITION_INFO

A <a href="https://msdn.microsoft.com/656b230d-b4ba-45e4-b6b3-8bbe72f9428a">CLUS_PARTITION_INFO</a> structure.


#### - szFileSystem

Member of the <a href="https://msdn.microsoft.com/656b230d-b4ba-45e4-b6b3-8bbe72f9428a">CLUS_PARTITION_INFO</a> structure 
       that describes the name of the file system, such as "FAT" or "NTFS".


## -see-also




<a href="https://msdn.microsoft.com/54597c05-57af-49ad-96e0-171f09c45a65">CLUSPROP_PIFLAGS</a>



<a href="https://msdn.microsoft.com/23353e11-63bb-4d3b-90fb-e2a5544e0d09">CLUSPROP_SYNTAX</a>



<a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a>



<a href="https://msdn.microsoft.com/656b230d-b4ba-45e4-b6b3-8bbe72f9428a">CLUS_PARTITION_INFO</a>



<a href="https://msdn.microsoft.com/e3ad7c34-0c8a-4f03-8e5c-b57802c493f0">Data structures</a>
 

 

