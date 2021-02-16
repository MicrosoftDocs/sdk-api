---
UID: NS:iprtrmib._MIB_OPAQUE_QUERY
title: MIB_OPAQUE_QUERY (iprtrmib.h)
description: Contains information for a MIB opaque query.
helpviewer_keywords: ["*PMIB_OPAQUE_QUERY","MIB_OPAQUE_QUERY","MIB_OPAQUE_QUERY structure [MIB]","PMIB_OPAQUE_QUERY","PMIB_OPAQUE_QUERY structure pointer [MIB]","_mpr_mib_opaque_query","iprtrmib/MIB_OPAQUE_QUERY","iprtrmib/PMIB_OPAQUE_QUERY","mib.mib_opaque_query","rras.mib_opaque_query"]
old-location: mib\mib_opaque_query.htm
tech.root: MIB
ms.assetid: cd87cbe4-3da4-4205-9a88-becf4f341ab5
ms.date: 12/05/2018
ms.keywords: '*PMIB_OPAQUE_QUERY, MIB_OPAQUE_QUERY, MIB_OPAQUE_QUERY structure [MIB], PMIB_OPAQUE_QUERY, PMIB_OPAQUE_QUERY structure pointer [MIB], _mpr_mib_opaque_query, iprtrmib/MIB_OPAQUE_QUERY, iprtrmib/PMIB_OPAQUE_QUERY, mib.mib_opaque_query, rras.mib_opaque_query'
req.header: iprtrmib.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: MIB_OPAQUE_QUERY, *PMIB_OPAQUE_QUERY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIB_OPAQUE_QUERY
 - iprtrmib/_MIB_OPAQUE_QUERY
 - PMIB_OPAQUE_QUERY
 - iprtrmib/PMIB_OPAQUE_QUERY
 - MIB_OPAQUE_QUERY
 - iprtrmib/MIB_OPAQUE_QUERY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iprtrmib.h
api_name:
 - MIB_OPAQUE_QUERY
---

# MIB_OPAQUE_QUERY structure


## -description

The 
<b>MIB_OPAQUE_QUERY</b> structure contains information for a MIB opaque query.

## -struct-fields

### -field dwVarId

The identifier of the MIB object to query.

### -field rgdwVarIndex

The index of the MIB object to query.

## -see-also

<a href="/windows/desktop/api/iprtrmib/ns-iprtrmib-mib_opaque_info">MIB_OPAQUE_INFO</a>