---
UID: NS:winnt._CACHE_DESCRIPTOR
title: CACHE_DESCRIPTOR (winnt.h)
description: Describes the cache attributes.
helpviewer_keywords: ["*PCACHE_DESCRIPTOR","CACHE_DESCRIPTOR","CACHE_DESCRIPTOR structure","PCACHE_DESCRIPTOR","PCACHE_DESCRIPTOR structure pointer","_CACHE_DESCRIPTOR","base.cache_descriptor","winnt/CACHE_DESCRIPTOR","winnt/PCACHE_DESCRIPTOR"]
old-location: base\cache_descriptor.htm
tech.root: backup
ms.assetid: 38cfa605-831c-45ef-a99f-55f42b2b56e9
ms.date: 12/05/2018
ms.keywords: '*PCACHE_DESCRIPTOR, CACHE_DESCRIPTOR, CACHE_DESCRIPTOR structure, PCACHE_DESCRIPTOR, PCACHE_DESCRIPTOR structure pointer, _CACHE_DESCRIPTOR, base.cache_descriptor, winnt/CACHE_DESCRIPTOR, winnt/PCACHE_DESCRIPTOR'
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP Professional x64 Edition [desktop apps only]
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
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
req.typenames: CACHE_DESCRIPTOR, *PCACHE_DESCRIPTOR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CACHE_DESCRIPTOR
 - winnt/_CACHE_DESCRIPTOR
 - PCACHE_DESCRIPTOR
 - winnt/PCACHE_DESCRIPTOR
 - CACHE_DESCRIPTOR
 - winnt/CACHE_DESCRIPTOR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinNT.h
api_name:
 - CACHE_DESCRIPTOR
---

# CACHE_DESCRIPTOR structure


## -description

Describes the cache attributes.

## -struct-fields

### -field Level

The cache level. This member can currently be one of the following values; other values may be supported in the future.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
L1

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2</dt>
</dl>
</td>
<td width="60%">
L2

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>3</dt>
</dl>
</td>
<td width="60%">
L3

</td>
</tr>
</table>

### -field Associativity

The cache associativity. If this member is CACHE_FULLY_ASSOCIATIVE (0xFF), the cache is fully associative.

### -field LineSize

The cache line size, in bytes.

### -field Size

The cache size, in bytes.

### -field Type

The cache type. This member is a <a href="/windows/desktop/api/winnt/ne-winnt-processor_cache_type">PROCESSOR_CACHE_TYPE</a> value.

## -see-also

<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation">GetLogicalProcessorInformation</a>



<a href="/windows/desktop/api/winnt/ne-winnt-processor_cache_type">PROCESSOR_CACHE_TYPE</a>



<a href="/windows/desktop/api/winnt/ns-winnt-system_logical_processor_information">SYSTEM_LOGICAL_PROCESSOR_INFORMATION</a>