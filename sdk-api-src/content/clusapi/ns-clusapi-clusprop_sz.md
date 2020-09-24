---
UID: NS:clusapi.CLUSPROP_SZ
title: CLUSPROP_SZ (clusapi.h)
description: Describes multiple NULL-terminated Unicode strings.
helpviewer_keywords: ["*PCLUSPROP_MULTI_SZ","*PCLUSPROP_PROPERTY_NAME","*PCLUSPROP_SZ","CLUSPROP_MULTI_SZ","CLUSPROP_MULTI_SZ structure [Failover Cluster]","CLUSPROP_PROPERTY_NAME","CLUSPROP_SZ","PCLUSPROP_MULTI_SZ","PCLUSPROP_MULTI_SZ structure pointer [Failover Cluster]","_wolf_clusprop_multi_sz","clusapi/CLUSPROP_MULTI_SZ","clusapi/PCLUSPROP_MULTI_SZ","mscs.clusprop_multi_sz"]
old-location: mscs\clusprop_multi_sz.htm
tech.root: MsCS
ms.assetid: 3c508ed6-eec8-4fa9-9ae7-9c8d7f4c8b98
ms.date: 12/05/2018
ms.keywords: '*PCLUSPROP_MULTI_SZ, *PCLUSPROP_PROPERTY_NAME, *PCLUSPROP_SZ, CLUSPROP_MULTI_SZ, CLUSPROP_MULTI_SZ structure [Failover Cluster], CLUSPROP_PROPERTY_NAME, CLUSPROP_SZ, PCLUSPROP_MULTI_SZ, PCLUSPROP_MULTI_SZ structure pointer [Failover Cluster], _wolf_clusprop_multi_sz, clusapi/CLUSPROP_MULTI_SZ, clusapi/PCLUSPROP_MULTI_SZ, mscs.clusprop_multi_sz'
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
req.typenames: CLUSPROP_SZ, *PCLUSPROP_SZ
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSPROP_SZ
 - clusapi/CLUSPROP_SZ
 - PCLUSPROP_SZ
 - clusapi/PCLUSPROP_SZ
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
 - CLUSPROP_MULTI_SZ
---

## -description

Describes multiple 
    <b>NULL</b>-terminated Unicode strings. It is used as an entry in a 
    <a href="/previous-versions/windows/desktop/mscs/value-lists">value list</a> and consists of:
<ul>
<li>A <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_value">CLUSPROP_VALUE</a> structure describing the format, 
     type, and length of the partition information.</li>
<li>A string array.</li>
</ul>For convenience, the <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_value">CLUSPROP_VALUE</a> members are listed 
    explicitly.

## -struct-fields

### -field sz

Multiple null-terminated Unicode strings with the last string followed by an additional <b>NULL</b>-terminating character.

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_syntax">CLUSPROP_SYNTAX</a>

<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_value">CLUSPROP_VALUE</a>

<a href="/previous-versions/windows/desktop/mscs/data-structures">Data structures</a>