---
UID: NS:clusapi.CLUSPROP_WORD
title: CLUSPROP_WORD (clusapi.h)
description: Describes numeric data.
helpviewer_keywords: ["*PCLUSPROP_WORD","CLUSPROP_WORD","CLUSPROP_WORD structure [Failover Cluster]","PCLUSPROP_WORD","PCLUSPROP_WORD structure pointer [Failover Cluster]","_wolf_clusprop_word","clusapi/CLUSPROP_WORD","clusapi/PCLUSPROP_WORD","mscs.clusprop_word"]
old-location: mscs\clusprop_word.htm
tech.root: MsCS
ms.assetid: ba09290b-171b-45cf-a367-485f7322ebef
ms.date: 12/05/2018
ms.keywords: '*PCLUSPROP_WORD, CLUSPROP_WORD, CLUSPROP_WORD structure [Failover Cluster], PCLUSPROP_WORD, PCLUSPROP_WORD structure pointer [Failover Cluster], _wolf_clusprop_word, clusapi/CLUSPROP_WORD, clusapi/PCLUSPROP_WORD, mscs.clusprop_word'
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
req.typenames: CLUSPROP_WORD, *PCLUSPROP_WORD
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSPROP_WORD
 - clusapi/CLUSPROP_WORD
 - PCLUSPROP_WORD
 - clusapi/PCLUSPROP_WORD
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
 - CLUSPROP_WORD
---

# CLUSPROP_WORD structure


## -description

Describes numeric data. It 
    is used as an entry in a <a href="/previous-versions/windows/desktop/mscs/value-lists">value list</a> and consists of:
<ul>
<li>A <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_value">CLUSPROP_VALUE</a> structure describing the format, 
     type, and length of the numeric data.</li>
<li>A <b>WORD</b> value.</li>
</ul>

## -struct-fields

### -field w

Numeric value.

### -field CLUSPROP_VALUE

<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_value">CLUSPROP_VALUE</a> structure describing 
       the format, type, and 
       the count of bytes in the <b>w</b> member.

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_syntax">CLUSPROP_SYNTAX</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_value">CLUSPROP_VALUE</a>



<a href="/previous-versions/windows/desktop/mscs/data-structures">Data structures</a>