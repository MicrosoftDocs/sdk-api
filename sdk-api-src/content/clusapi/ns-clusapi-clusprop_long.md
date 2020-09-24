---
UID: NS:clusapi.CLUSPROP_LONG
title: CLUSPROP_LONG (clusapi.h)
description: Describes signed LONG data.
helpviewer_keywords: ["*PCLUSPROP_LONG","CLUSPROP_LONG","CLUSPROP_LONG structure [Failover Cluster]","PCLUSPROP_LONG","PCLUSPROP_LONG structure pointer [Failover Cluster]","_wolf_clusprop_long","clusapi/CLUSPROP_LONG","clusapi/PCLUSPROP_LONG","mscs.clusprop_long"]
old-location: mscs\clusprop_long.htm
tech.root: MsCS
ms.assetid: aa214e43-cadc-4f06-8c98-e6a5b13258b8
ms.date: 12/05/2018
ms.keywords: '*PCLUSPROP_LONG, CLUSPROP_LONG, CLUSPROP_LONG structure [Failover Cluster], PCLUSPROP_LONG, PCLUSPROP_LONG structure pointer [Failover Cluster], _wolf_clusprop_long, clusapi/CLUSPROP_LONG, clusapi/PCLUSPROP_LONG, mscs.clusprop_long'
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
req.typenames: CLUSPROP_LONG, *PCLUSPROP_LONG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSPROP_LONG
 - clusapi/CLUSPROP_LONG
 - PCLUSPROP_LONG
 - clusapi/PCLUSPROP_LONG
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
 - CLUSPROP_LONG
---

# CLUSPROP_LONG structure


## -description

Describes signed 
    <b>LONG</b> data. It is used as an entry in a 
    <a href="/previous-versions/windows/desktop/mscs/value-lists">value list</a> and consists of:
<ul>
<li>A <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_value">CLUSPROP_VALUE</a> structure describing the format, 
     type, and length of the numeric data.</li>
<li>A <b>LONG</b> value.</li>
</ul>

## -struct-fields

### -field l

Signed <b>LONG</b> value.

### -field CLUSPROP_VALUE

<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_value">CLUSPROP_VALUE</a> structure with a <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_syntax">CLUSPROP_SYNTAX</a>  with a value 
       of <b>CLUSPROP_SYNTAX_LIST_VALUE_LONG</b> (0x00010007) and a <b>cbLength</b> field indicating 
       the count of bytes in the <b>l</b> member.

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_syntax">CLUSPROP_SYNTAX</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_value">CLUSPROP_VALUE</a>



<a href="/previous-versions/windows/desktop/mscs/data-structures">Data structures</a>