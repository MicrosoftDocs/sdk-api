---
UID: NE:winnt._PROCESSOR_CACHE_TYPE
title: "_PROCESSOR_CACHE_TYPE"
author: windows-sdk-content
description: Represents the type of processor cache identified in the corresponding CACHE_DESCRIPTOR structure.
old-location: base\processor_cache_type.htm
tech.root: procthread
ms.assetid: 23044f67-e944-43c2-8c75-3d2fba87cb3c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CacheData, CacheInstruction, CacheTrace, CacheUnified, PROCESSOR_CACHE_TYPE, PROCESSOR_CACHE_TYPE enumeration, _PROCESSOR_CACHE_TYPE, base.processor_cache_type, winnt/CacheData, winnt/CacheInstruction, winnt/CacheTrace, winnt/CacheUnified, winnt/PROCESSOR_CACHE_TYPE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinNT.h
api_name:
 - PROCESSOR_CACHE_TYPE
product: Windows
targetos: Windows
req.typenames: PROCESSOR_CACHE_TYPE
req.redist: 
---

# _PROCESSOR_CACHE_TYPE enumeration


## -description


Represents the type of processor cache identified in the corresponding <a href="https://msdn.microsoft.com/38cfa605-831c-45ef-a99f-55f42b2b56e9">CACHE_DESCRIPTOR</a> structure.


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




<a href="https://msdn.microsoft.com/38cfa605-831c-45ef-a99f-55f42b2b56e9">CACHE_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/904d2d35-f419-4e8f-a689-f39ed926644c">GetLogicalProcessorInformation</a>



<a href="https://msdn.microsoft.com/32ef5dd8-c00d-44ee-a291-a18653beb1b9">SYSTEM_LOGICAL_PROCESSOR_INFORMATION</a>
 

 

