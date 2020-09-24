---
UID: NS:clusapi.CLUSPROP_VALUE
title: CLUSPROP_VALUE (clusapi.h)
description: Describes the syntax and length of a data value used in a value list. The CLUSPROP_VALUE structure is used as a generic header in all of the structures that describe data of a particular type, such as CLUSPROP_BINARY and CLUSPROP_SZ.
helpviewer_keywords: ["*PCLUSPROP_VALUE","CLUSPROP_VALUE","CLUSPROP_VALUE structure [Failover Cluster]","PCLUSPROP_VALUE","PCLUSPROP_VALUE structure pointer [Failover Cluster]","_wolf_clusprop_value","clusapi/CLUSPROP_VALUE","clusapi/PCLUSPROP_VALUE","mscs.clusprop_value"]
old-location: mscs\clusprop_value.htm
tech.root: MsCS
ms.assetid: a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd
ms.date: 12/05/2018
ms.keywords: '*PCLUSPROP_VALUE, CLUSPROP_VALUE, CLUSPROP_VALUE structure [Failover Cluster], PCLUSPROP_VALUE, PCLUSPROP_VALUE structure pointer [Failover Cluster], _wolf_clusprop_value, clusapi/CLUSPROP_VALUE, clusapi/PCLUSPROP_VALUE, mscs.clusprop_value'
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
req.typenames: CLUSPROP_VALUE, *PCLUSPROP_VALUE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSPROP_VALUE
 - clusapi/CLUSPROP_VALUE
 - PCLUSPROP_VALUE
 - clusapi/PCLUSPROP_VALUE
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
 - CLUSPROP_VALUE
---

# CLUSPROP_VALUE structure


## -description

Describes the syntax and 
    length of a data value used in a <a href="/previous-versions/windows/desktop/mscs/value-lists">value list</a>. The 
    <b>CLUSPROP_VALUE</b> structure is used as a generic header in 
    all of the structures that describe data of a particular type, such as 
    <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_binary">CLUSPROP_BINARY</a> and 
    <a href="/previous-versions/windows/desktop/legacy/aa368390(v=vs.85)">CLUSPROP_SZ</a>.

## -struct-fields

### -field Syntax

<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_syntax">CLUSPROP_SYNTAX</a> union that describes a 
      value.

### -field cbLength

Count of bytes in the data that follows this 
      <b>CLUSPROP_VALUE</b> structure.

## -remarks

The <b>CLUSPROP_VALUE</b> structure is used to describe the 
     format, type, and length of a data value in the following structures:

<ul>
<li>
<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_binary">CLUSPROP_BINARY</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_dword">CLUSPROP_DISK_NUMBER</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/legacy/aa368374(v=vs.85)">CLUSPROP_DISK_SIGNATURE</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/legacy/aa368375(v=vs.85)">CLUSPROP_DWORD</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_filetime">CLUSPROP_FILETIME</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_long">CLUSPROP_LONG</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_sz">CLUSPROP_MULTI_SZ</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_partition_info">CLUSPROP_PARTITION_INFO</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_partition_info_ex">CLUSPROP_PARTITION_INFO_EX</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/legacy/aa368382(v=vs.85)">CLUSPROP_PROPERTY_NAME</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_required_dependency">CLUSPROP_REQUIRED_DEPENDENCY</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_resource_class">CLUSPROP_RESOURCE_CLASS</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_resource_class_info">CLUSPROP_RESOURCE_CLASS_INFO</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_scsi_address">CLUSPROP_SCSI_ADDRESS</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/legacy/aa368390(v=vs.85)">CLUSPROP_SZ</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_ularge_integer">CLUSPROP_ULARGE_INTEGER</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_word">CLUSPROP_WORD</a>
</li>
</ul>

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_binary">CLUSPROP_BINARY</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_syntax">CLUSPROP_SYNTAX</a>



<a href="/previous-versions/windows/desktop/legacy/aa368390(v=vs.85)">CLUSPROP_SZ</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_value">CLUSPROP_VALUE</a>



<a href="/previous-versions/windows/desktop/mscs/data-structures">Data structures</a>