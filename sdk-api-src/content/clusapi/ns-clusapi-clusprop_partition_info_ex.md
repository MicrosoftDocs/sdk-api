---
UID: NS:clusapi.CLUSPROP_PARTITION_INFO_EX
title: CLUSPROP_PARTITION_INFO_EX (clusapi.h)
author: windows-sdk-content
description: The CLUSPROP_PARTITION_INFO_EX structure contains information relevant to storage class resources.
old-location: mscs\clusprop_partition_info_ex.htm
tech.root: MsCS
ms.assetid: b1343a04-b8bd-469a-a620-985eeb89401c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PCLUSPROP_PARTITION_INFO_EX, CLUSPROP_PARTITION_INFO_EX, CLUSPROP_PARTITION_INFO_EX structure [Failover Cluster], PCLUSPROP_PARTITION_INFO_EX, PCLUSPROP_PARTITION_INFO_EX structure pointer [Failover Cluster], clusapi/CLUSPROP_PARTITION_INFO_EX, clusapi/PCLUSPROP_PARTITION_INFO_EX, mscs.clusprop_partition_info_ex"
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
 - ClusAPI.h
api_name:
 - CLUSPROP_PARTITION_INFO_EX
product: Windows
targetos: Windows
req.typenames: CLUSPROP_PARTITION_INFO_EX
req.redist: 
ms.custom: 19H1
---

# CLUSPROP_PARTITION_INFO_EX structure


## -description


Specifies a collection of information about a physical disk resource, such as its device name and volume label. 
    The <b>CLUSPROP_PARTITION_INFO_EX</b> 
    structure contains information relevant to 
    <a href="https://msdn.microsoft.com/en-us/library/Aa372937(v=VS.85).aspx">storage class resources</a>. It is 
    used as an entry in a <a href="https://msdn.microsoft.com/f2b20fe5-0d7e-4ccd-b288-aa8104a24fef">value list</a> and consists of:
<ul>
<li>A <a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> structure describing the format, 
     type, and length of the partition information.</li>
<li>A <a href="https://msdn.microsoft.com/d061bcb5-7c4c-4d07-9cdf-fa9f7ac34b3c">CLUS_PARTITION_INFO_EX</a> 
     structure.</li>
</ul>

## -struct-fields




### -field CLUSPROP_VALUE


<a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> structure with a <a href="https://msdn.microsoft.com/23353e11-63bb-4d3b-90fb-e2a5544e0d09">CLUSPROP_SYNTAX</a>  with a value 
       of <b>CLUSPROP_SYNTAX_PARTITION_INFO_EX</b> (0x000d0001) and a <b>cbLength</b> field indicating 
       the count of bytes in the <b>CLUS_PARTITION_INFO_EX</b> member.


### -field CLUS_PARTITION_INFO_EX

A <a href="https://msdn.microsoft.com/d061bcb5-7c4c-4d07-9cdf-fa9f7ac34b3c">CLUS_PARTITION_INFO_EX</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/cda1e334-dba8-4fe9-b035-4e475245869c">CLUSPROP_PARTITION_INFO</a>



<a href="https://msdn.microsoft.com/54597c05-57af-49ad-96e0-171f09c45a65">CLUSPROP_PIFLAGS</a>



<a href="https://msdn.microsoft.com/23353e11-63bb-4d3b-90fb-e2a5544e0d09">CLUSPROP_SYNTAX</a>



<a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a>



<a href="https://msdn.microsoft.com/d061bcb5-7c4c-4d07-9cdf-fa9f7ac34b3c">CLUS_PARTITION_INFO_EX</a>



<a href="https://msdn.microsoft.com/e3ad7c34-0c8a-4f03-8e5c-b57802c493f0">Data structures</a>
 

 

