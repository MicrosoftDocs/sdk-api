---
UID: NS:clusapi.CLUSPROP_FILETIME
title: CLUSPROP_FILETIME (clusapi.h)
description: Describes a date and time stamp for a file.
helpviewer_keywords: ["*PCLUSPROP_FILETIME","CLUSPROP_FILETIME","CLUSPROP_FILETIME structure [Failover Cluster]","PCLUSPROP_FILETIME","PCLUSPROP_FILETIME structure pointer [Failover Cluster]","clusapi/CLUSPROP_FILETIME","clusapi/PCLUSPROP_FILETIME","mscs.clusprop_filetime"]
old-location: mscs\clusprop_filetime.htm
tech.root: MsCS
ms.assetid: 2c88e9db-f218-4b88-9bb0-607fd09e8d0b
ms.date: 12/05/2018
ms.keywords: '*PCLUSPROP_FILETIME, CLUSPROP_FILETIME, CLUSPROP_FILETIME structure [Failover Cluster], PCLUSPROP_FILETIME, PCLUSPROP_FILETIME structure pointer [Failover Cluster], clusapi/CLUSPROP_FILETIME, clusapi/PCLUSPROP_FILETIME, mscs.clusprop_filetime'
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
req.typenames: CLUSPROP_FILETIME, *PCLUSPROP_FILETIME
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSPROP_FILETIME
 - clusapi/CLUSPROP_FILETIME
 - PCLUSPROP_FILETIME
 - clusapi/PCLUSPROP_FILETIME
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
 - CLUSPROP_FILETIME
---

# CLUSPROP_FILETIME structure


## -description

Describes a date 
     and time stamp for a file. It is used as an entry in a 
     <a href="/previous-versions/windows/desktop/mscs/value-lists">value list</a> and consists of:
<ul>
<li>A <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_value">CLUSPROP_VALUE</a> structure indicating the format 
      and type of the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> value.</li>
<li>A <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> value.</li>
</ul>For convenience, the <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_value">CLUSPROP_VALUE</a> members are listed 
     explicitly.

## -struct-fields

### -field ft

A date and time value.

### -field CLUSPROP_VALUE

<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_value">CLUSPROP_VALUE</a> structure with a <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_syntax">CLUSPROP_SYNTAX</a>  with a value 
       of <b>CLUSPROP_SYNTAX_LIST_VALUE_FILETIME</b> (0x0001000c) and a <b>cbLength</b> field indicating 
       the count of bytes in the <b>ft</b> member.

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_syntax">CLUSPROP_SYNTAX</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_value">CLUSPROP_VALUE</a>



<a href="/previous-versions/windows/desktop/mscs/data-structures">Data structures</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>