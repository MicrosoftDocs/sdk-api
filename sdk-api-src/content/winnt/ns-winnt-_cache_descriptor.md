---
UID: NS:winnt._CACHE_DESCRIPTOR
title: "_CACHE_DESCRIPTOR"
author: windows-sdk-content
description: Describes the cache attributes.
old-location: base\cache_descriptor.htm
tech.root: procthread
ms.assetid: 38cfa605-831c-45ef-a99f-55f42b2b56e9
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: "*PCACHE_DESCRIPTOR, CACHE_DESCRIPTOR, CACHE_DESCRIPTOR structure, PCACHE_DESCRIPTOR, PCACHE_DESCRIPTOR structure pointer, _CACHE_DESCRIPTOR, base.cache_descriptor, winnt/CACHE_DESCRIPTOR, winnt/PCACHE_DESCRIPTOR"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
 - CACHE_DESCRIPTOR
product: Windows
targetos: Windows
req.typenames: CACHE_DESCRIPTOR, *PCACHE_DESCRIPTOR
req.redist: 
---

# _CACHE_DESCRIPTOR structure


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

The cache type. This member is a <a href="https://msdn.microsoft.com/23044f67-e944-43c2-8c75-3d2fba87cb3c">PROCESSOR_CACHE_TYPE</a> value.


## -see-also




<a href="https://msdn.microsoft.com/904d2d35-f419-4e8f-a689-f39ed926644c">GetLogicalProcessorInformation</a>



<a href="https://msdn.microsoft.com/23044f67-e944-43c2-8c75-3d2fba87cb3c">PROCESSOR_CACHE_TYPE</a>



<a href="https://msdn.microsoft.com/32ef5dd8-c00d-44ee-a291-a18653beb1b9">SYSTEM_LOGICAL_PROCESSOR_INFORMATION</a>
 

 

