---
UID: NS:winnt._CACHE_RELATIONSHIP
title: "_CACHE_RELATIONSHIP"
author: windows-sdk-content
description: Describes cache attributes. This structure is used with the GetLogicalProcessorInformationEx function.
old-location: base\cache_relationship.htm
tech.root: procthread
ms.assetid: f8fe521b-02d6-4c58-8ef8-653280add111
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*PCACHE_RELATIONSHIP, CACHE_RELATIONSHIP, CACHE_RELATIONSHIP structure, PCACHE_RELATIONSHIP, PCACHE_RELATIONSHIP structure pointer, _CACHE_RELATIONSHIP, base.cache_relationship, winnt/CACHE_RELATIONSHIP, winnt/PCACHE_RELATIONSHIP"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winnt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - CACHE_RELATIONSHIP
product: Windows
targetos: Windows
req.typenames: CACHE_RELATIONSHIP, *PCACHE_RELATIONSHIP
req.redist: 
---

# _CACHE_RELATIONSHIP structure


## -description


Describes cache attributes. This structure is used with the <a href="https://msdn.microsoft.com/dfc4f444-4651-4a02-b8f6-f30d9278eae2">GetLogicalProcessorInformationEx</a> function.


## -struct-fields




### -field Level

The cache level. This member can be one of the following values.

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


### -field CacheSize

The cache size, in bytes.


### -field Type

The cache type. This member is a <a href="https://msdn.microsoft.com/23044f67-e944-43c2-8c75-3d2fba87cb3c">PROCESSOR_CACHE_TYPE</a> value.


### -field Reserved

This member is reserved.


### -field GroupMask

A <a href="https://msdn.microsoft.com/76009431-9139-4c03-9c7b-0c4bb5f0cb83">GROUP_AFFINITY</a> structure that specifies a  group number and processor affinity within the group. 


## -see-also




<a href="https://msdn.microsoft.com/76009431-9139-4c03-9c7b-0c4bb5f0cb83">GROUP_AFFINITY</a>



<a href="https://msdn.microsoft.com/dfc4f444-4651-4a02-b8f6-f30d9278eae2">GetLogicalProcessorInformationEx</a>



<a href="https://msdn.microsoft.com/23044f67-e944-43c2-8c75-3d2fba87cb3c">PROCESSOR_CACHE_TYPE</a>



<a href="https://msdn.microsoft.com/6ff16cda-c1dc-4d5c-ac60-756653cd6b07">SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX</a>
 

 

