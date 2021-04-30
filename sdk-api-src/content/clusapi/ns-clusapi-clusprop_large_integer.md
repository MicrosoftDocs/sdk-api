---
UID: NS:clusapi.CLUSPROP_LARGE_INTEGER
title: CLUSPROP_LARGE_INTEGER (clusapi.h)
description: Describes a signed large integer.
helpviewer_keywords: ["*PCLUSPROP_LARGE_INTEGER","CLUSPROP_LARGE_INTEGER","CLUSPROP_LARGE_INTEGER structure [Failover Cluster]","PCLUSPROP_LARGE_INTEGER","PCLUSPROP_LARGE_INTEGER structure pointer [Failover Cluster]","_wolf_clusprop_large_integer","clusapi/CLUSPROP_LARGE_INTEGER","clusapi/PCLUSPROP_LARGE_INTEGER","mscs.clusprop_large_integer"]
old-location: mscs\clusprop_large_integer.htm
tech.root: MsCS
ms.assetid: 3e0849e6-3d93-47cb-858d-9891451b8dfd
ms.date: 10/15/2020
ms.keywords: '*PCLUSPROP_LARGE_INTEGER, CLUSPROP_LARGE_INTEGER, CLUSPROP_LARGE_INTEGER structure [Failover Cluster], PCLUSPROP_LARGE_INTEGER, PCLUSPROP_LARGE_INTEGER structure pointer [Failover Cluster], _wolf_clusprop_large_integer, clusapi/CLUSPROP_LARGE_INTEGER, clusapi/PCLUSPROP_LARGE_INTEGER, mscs.clusprop_large_integer'
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
req.typenames: CLUSPROP_LARGE_INTEGER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSPROP_LARGE_INTEGER
 - clusapi/CLUSPROP_LARGE_INTEGER
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
 - CLUSPROP_LARGE_INTEGER
---

# CLUSPROP_LARGE_INTEGER structure


## -description

Describes a signed large integer. It is used as an entry in a <a href="/previous-versions/windows/desktop/mscs/value-lists">value list</a> and consists of:
<ul>
<li>A <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_value">CLUSPROP_VALUE</a> structure indicating the format and type of the integer value.</li>
<li>Assigned large integer value.</li>
</ul>

## -struct-fields

### -field li

Signed large integer value.

### -field CLUSPROP_VALUE

<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_value">CLUSPROP_VALUE</a> structure with a  <b>cbLength</b> field indicating 
       the count of bytes in the <b>li</b> member.

## -remarks

Use caution when referencing large integer values in <b>DWORD</b>-aligned structures such 
     as value lists, <a href="/previous-versions/windows/desktop/mscs/property-lists">property lists</a>, and 
     <a href="/previous-versions/windows/desktop/mscs/parameter-blocks">parameter blocks</a>. For Windows Server for Itanium-based 
     systems, a naturally-aligned large integer value always begins on an address ending in 0h or 8h. 
     <b>DWORD</b>-alignment can cause large values to begin on unaligned boundaries (addresses 
     ending in 4h or Ch), which will cause an alignment fault when the data is read or written. You can avoid 
     alignment faults by separately copying the high and low <b>DWORD</b>s of large values into 
     local variables, which are guaranteed to be naturally aligned.

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_syntax">CLUSPROP_SYNTAX</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_value">CLUSPROP_VALUE</a>



<a href="/previous-versions/windows/desktop/mscs/data-structures">Data structures</a>



<a href="/windows/win32/api/winnt/ns-winnt-large_integer-r1">LARGE_INTEGER</a>
