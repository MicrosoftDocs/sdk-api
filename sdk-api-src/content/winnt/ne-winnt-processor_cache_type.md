---
UID: NE:winnt._PROCESSOR_CACHE_TYPE
title: PROCESSOR_CACHE_TYPE (winnt.h)
description: Represents the type of processor cache identified in the corresponding CACHE_DESCRIPTOR structure.
helpviewer_keywords: ["CacheData","CacheInstruction","CacheTrace","CacheUnified","PROCESSOR_CACHE_TYPE","PROCESSOR_CACHE_TYPE enumeration","base.processor_cache_type","winnt/CacheData","winnt/CacheInstruction","winnt/CacheTrace","winnt/CacheUnified","winnt/PROCESSOR_CACHE_TYPE"]
old-location: base\processor_cache_type.htm
tech.root: backup
ms.assetid: 23044f67-e944-43c2-8c75-3d2fba87cb3c
ms.date: 12/05/2018
ms.keywords: CacheData, CacheInstruction, CacheTrace, CacheUnified, PROCESSOR_CACHE_TYPE, PROCESSOR_CACHE_TYPE enumeration, base.processor_cache_type, winnt/CacheData, winnt/CacheInstruction, winnt/CacheTrace, winnt/CacheUnified, winnt/PROCESSOR_CACHE_TYPE
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
req.typenames: PROCESSOR_CACHE_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PROCESSOR_CACHE_TYPE
 - winnt/_PROCESSOR_CACHE_TYPE
 - PROCESSOR_CACHE_TYPE
 - winnt/PROCESSOR_CACHE_TYPE
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
 - PROCESSOR_CACHE_TYPE
---

# PROCESSOR_CACHE_TYPE enumeration


## -description

Represents the type of processor cache identified in the corresponding <a href="/windows/desktop/api/winnt/ns-winnt-cache_descriptor">CACHE_DESCRIPTOR</a> structure.

## -enum-fields

### -field CacheUnified

The cache is unified.

### -field CacheInstruction

The cache is for processor instructions.

### -field CacheData

The cache is for data.

### -field CacheTrace

The cache is for traces.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-cache_descriptor">CACHE_DESCRIPTOR</a>



<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation">GetLogicalProcessorInformation</a>



<a href="/windows/desktop/api/winnt/ns-winnt-system_logical_processor_information">SYSTEM_LOGICAL_PROCESSOR_INFORMATION</a>