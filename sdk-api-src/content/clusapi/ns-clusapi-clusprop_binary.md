---
UID: NS:clusapi.CLUSPROP_BINARY
title: CLUSPROP_BINARY (clusapi.h)
description: Describes a binary data value.
helpviewer_keywords: ["*PCLUSPROP_BINARY","CLUSPROP_BINARY","CLUSPROP_BINARY structure [Failover Cluster]","PCLUSPROP_BINARY","PCLUSPROP_BINARY structure pointer [Failover Cluster]","_wolf_clusprop_binary","clusapi/CLUSPROP_BINARY","clusapi/PCLUSPROP_BINARY","mscs.clusprop_binary"]
old-location: mscs\clusprop_binary.htm
tech.root: MsCS
ms.assetid: 61169871-4998-4e9f-97dc-77344bbfa962
ms.date: 12/05/2018
ms.keywords: '*PCLUSPROP_BINARY, CLUSPROP_BINARY, CLUSPROP_BINARY structure [Failover Cluster], PCLUSPROP_BINARY, PCLUSPROP_BINARY structure pointer [Failover Cluster], _wolf_clusprop_binary, clusapi/CLUSPROP_BINARY, clusapi/PCLUSPROP_BINARY, mscs.clusprop_binary'
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
req.typenames: CLUSPROP_BINARY, *PCLUSPROP_BINARY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSPROP_BINARY
 - clusapi/CLUSPROP_BINARY
 - PCLUSPROP_BINARY
 - clusapi/PCLUSPROP_BINARY
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
 - CLUSPROP_BINARY
---

# CLUSPROP_BINARY structure


## -description

Describes a binary data value. It is used as an entry in a 
    <a href="/previous-versions/windows/desktop/mscs/value-lists">value list</a> and consists of:
<ul>
<li>A <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_value">CLUSPROP_VALUE</a> structure with a value 
       of <b>CLUSPROP_SYNTAX_LIST_VALUE_BINARY</b> (0x00010001).</li>
<li>A byte array containing the data.</li>
</ul>

## -struct-fields

### -field rgb

Array of bytes containing the data.

### -field CLUSPROP_VALUE

<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_value">CLUSPROP_VALUE</a> structure with a <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_syntax">CLUSPROP_SYNTAX</a>  with a value 
       of <b>CLUSPROP_SYNTAX_LIST_VALUE_BINARY</b> (0x00010001) and a <b>cbLength</b> field indicating 
       the count of bytes in the <b>rgb</b> member.

## -remarks

Use the <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusprop_binary_declare">CLUSPROP_BINARY_DECLARE</a> macro to 
     initialize a <b>CLUSPROP_BINARY</b> structure.

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusprop_binary_declare">CLUSPROP_BINARY_DECLARE</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_syntax">CLUSPROP_SYNTAX</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_value">CLUSPROP_VALUE</a>



<a href="/previous-versions/windows/desktop/mscs/data-structures">Data structures</a>