---
UID: NS:dbghelp._OMAP
title: OMAP (dbghelp.h)
description: Describes an entry in an address map.
helpviewer_keywords: ["*POMAP","OMAP","OMAP structure","POMAP","POMAP structure pointer","_OMAP","base.omap","dbghelp/OMAP","dbghelp/POMAP"]
old-location: base\omap.htm
tech.root: Debug
ms.assetid: 47f1dc1d-9305-4514-83b8-6d32bd9914f2
ms.date: 12/05/2018
ms.keywords: '*POMAP, OMAP, OMAP structure, POMAP, POMAP structure pointer, _OMAP, base.omap, dbghelp/OMAP, dbghelp/POMAP'
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: OMAP, *POMAP
req.redist: DbgHelp.dll 6.8 or later
ms.custom: 19H1
f1_keywords:
 - _OMAP
 - dbghelp/_OMAP
 - POMAP
 - dbghelp/POMAP
 - OMAP
 - dbghelp/OMAP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dbghelp.h
api_name:
 - OMAP
---

# OMAP structure


## -description

Describes an entry in an address map.

## -struct-fields

### -field rva

A relative virtual address (RVA) in image A.

### -field rvaTo

The relative virtual address that <b>rva</b> is mapped to in image B.

## -remarks

An address map provides a translation from one image layout (A) to another (B). An array of OMAP structures, sorted by <b>rva</b>, defines an address map.

To translate an address, addrA, in image A to an address, addrB, in image B, perform the following steps:

<ol>
<li>Search the map for the entry, e, with the largest rva less than or equal to addrA.</li>
<li>Set delta = addrA – e.rva.</li>
<li>Set addrB = e.rvaTo + delta.</li>
</ol>

## -see-also

<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgetomaps">SymGetOmaps</a>