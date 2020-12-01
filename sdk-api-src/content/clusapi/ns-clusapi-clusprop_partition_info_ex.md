---
UID: NS:clusapi.CLUSPROP_PARTITION_INFO_EX
title: CLUSPROP_PARTITION_INFO_EX (clusapi.h)
description: The CLUSPROP_PARTITION_INFO_EX structure contains information relevant to storage class resources.
helpviewer_keywords: ["*PCLUSPROP_PARTITION_INFO_EX","CLUSPROP_PARTITION_INFO_EX","CLUSPROP_PARTITION_INFO_EX structure [Failover Cluster]","PCLUSPROP_PARTITION_INFO_EX","PCLUSPROP_PARTITION_INFO_EX structure pointer [Failover Cluster]","clusapi/CLUSPROP_PARTITION_INFO_EX","clusapi/PCLUSPROP_PARTITION_INFO_EX","mscs.clusprop_partition_info_ex"]
old-location: mscs\clusprop_partition_info_ex.htm
tech.root: MsCS
ms.assetid: b1343a04-b8bd-469a-a620-985eeb89401c
ms.date: 12/05/2018
ms.keywords: '*PCLUSPROP_PARTITION_INFO_EX, CLUSPROP_PARTITION_INFO_EX, CLUSPROP_PARTITION_INFO_EX structure [Failover Cluster], PCLUSPROP_PARTITION_INFO_EX, PCLUSPROP_PARTITION_INFO_EX structure pointer [Failover Cluster], clusapi/CLUSPROP_PARTITION_INFO_EX, clusapi/PCLUSPROP_PARTITION_INFO_EX, mscs.clusprop_partition_info_ex'
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
targetos: Windows
req.typenames: CLUSPROP_PARTITION_INFO_EX
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSPROP_PARTITION_INFO_EX
 - clusapi/CLUSPROP_PARTITION_INFO_EX
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
 - CLUSPROP_PARTITION_INFO_EX
---

# CLUSPROP_PARTITION_INFO_EX structure


## -description

Specifies a collection of information about a physical disk resource, such as its device name and volume label. 
    The <b>CLUSPROP_PARTITION_INFO_EX</b> 
    structure contains information relevant to 
    <a href="/previous-versions/windows/desktop/mscs/s-gly">storage class resources</a>. It is 
    used as an entry in a <a href="/previous-versions/windows/desktop/mscs/value-lists">value list</a> and consists of:
<ul>
<li>A <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_value">CLUSPROP_VALUE</a> structure describing the format, 
     type, and length of the partition information.</li>
<li>A <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clus_partition_info_ex">CLUS_PARTITION_INFO_EX</a> 
     structure.</li>
</ul>

## -struct-fields

### -field CLUSPROP_VALUE

<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_value">CLUSPROP_VALUE</a> structure with a <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_syntax">CLUSPROP_SYNTAX</a>  with a value 
       of <b>CLUSPROP_SYNTAX_PARTITION_INFO_EX</b> (0x000d0001) and a <b>cbLength</b> field indicating 
       the count of bytes in the <b>CLUS_PARTITION_INFO_EX</b> member.

### -field CLUS_PARTITION_INFO_EX

A <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clus_partition_info_ex">CLUS_PARTITION_INFO_EX</a> structure.

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_partition_info">CLUSPROP_PARTITION_INFO</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-clusprop_piflags">CLUSPROP_PIFLAGS</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_syntax">CLUSPROP_SYNTAX</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_value">CLUSPROP_VALUE</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clus_partition_info_ex">CLUS_PARTITION_INFO_EX</a>



<a href="/previous-versions/windows/desktop/mscs/data-structures">Data structures</a>