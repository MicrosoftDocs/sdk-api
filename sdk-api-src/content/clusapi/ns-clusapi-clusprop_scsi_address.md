---
UID: NS:clusapi.CLUSPROP_SCSI_ADDRESS
title: CLUSPROP_SCSI_ADDRESS (clusapi.h)
description: Describes an address for a SCSI device.
helpviewer_keywords: ["*PCLUSPROP_SCSI_ADDRESS","CLUSPROP_SCSI_ADDRESS","CLUSPROP_SCSI_ADDRESS structure [Failover Cluster]","PCLUSPROP_SCSI_ADDRESS","PCLUSPROP_SCSI_ADDRESS structure pointer [Failover Cluster]","_wolf_clusprop_scsi_address","clusapi/CLUSPROP_SCSI_ADDRESS","clusapi/PCLUSPROP_SCSI_ADDRESS","mscs.clusprop_scsi_address"]
old-location: mscs\clusprop_scsi_address.htm
tech.root: MsCS
ms.assetid: 30907886-0c86-4e8a-9a95-5b62f6ffff76
ms.date: 12/05/2018
ms.keywords: '*PCLUSPROP_SCSI_ADDRESS, CLUSPROP_SCSI_ADDRESS, CLUSPROP_SCSI_ADDRESS structure [Failover Cluster], PCLUSPROP_SCSI_ADDRESS, PCLUSPROP_SCSI_ADDRESS structure pointer [Failover Cluster], _wolf_clusprop_scsi_address, clusapi/CLUSPROP_SCSI_ADDRESS, clusapi/PCLUSPROP_SCSI_ADDRESS, mscs.clusprop_scsi_address'
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
req.typenames: CLUSPROP_SCSI_ADDRESS, *PCLUSPROP_SCSI_ADDRESS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSPROP_SCSI_ADDRESS
 - clusapi/CLUSPROP_SCSI_ADDRESS
 - PCLUSPROP_SCSI_ADDRESS
 - clusapi/PCLUSPROP_SCSI_ADDRESS
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
 - CLUSPROP_SCSI_ADDRESS
---

# CLUSPROP_SCSI_ADDRESS structure


## -description

Describes an address for a <a href="/previous-versions/windows/desktop/mscs/s-gly">SCSI</a> 
    device. It is used as an entry in a <a href="/previous-versions/windows/desktop/mscs/value-lists">value list</a> and consists 
    of:
<ul>
<li>A <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_value">CLUSPROP_VALUE</a> structure indicating the format 
     and type of the resource class information.</li>
<li>A <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clus_scsi_address">CLUS_SCSI_ADDRESS</a> structure.</li>
</ul>For convenience, the <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_value">CLUSPROP_VALUE</a> and 
    <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clus_scsi_address">CLUS_SCSI_ADDRESS</a> members are listed explicitly.

## -struct-fields

### -field CLUSPROP_VALUE

<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_value">CLUSPROP_VALUE</a> structure with a <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_syntax">CLUSPROP_SYNTAX</a>  with a value 
       of <b>CLUSPROP_SYNTAX_SCSI_ADDRESS</b> (0x00060002) and a <b>cbLength</b> field indicating 
       the count of bytes in the <b>CLUS_SCSI_ADDRESS</b> member. Padding bytes are not included in the count.

### -field CLUS_SCSI_ADDRESS

A <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clus_scsi_address">CLUS_SCSI_ADDRESS</a> structure.

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_syntax">CLUSPROP_SYNTAX</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_value">CLUSPROP_VALUE</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clus_resource_class_info">CLUS_SCSI_ADDRESS</a>



<a href="/previous-versions/windows/desktop/mscs/clusscsiaddress-object">ClusScsiAddress</a>



<a href="/previous-versions/windows/desktop/mscs/data-structures">Data structures</a>