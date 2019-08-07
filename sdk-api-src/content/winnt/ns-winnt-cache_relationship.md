---
UID: NS:winnt._CACHE_RELATIONSHIP
title: CACHE_RELATIONSHIP (winnt.h)
author: windows-sdk-content
description: Describes cache attributes. This structure is used with the GetLogicalProcessorInformationEx function.
old-location: base\cache_relationship.htm
tech.root: ProcThread
ms.assetid: f8fe521b-02d6-4c58-8ef8-653280add111
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: '*PCACHE_RELATIONSHIP, CACHE_RELATIONSHIP, CACHE_RELATIONSHIP structure, PCACHE_RELATIONSHIP, PCACHE_RELATIONSHIP structure pointer, _CACHE_RELATIONSHIP, base.cache_relationship, winnt/CACHE_RELATIONSHIP, winnt/PCACHE_RELATIONSHIP'
ms.topic: struct
f1_keywords:
- winnt/CACHE_RELATIONSHIP
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
ms.custom: 19H1
---

# CACHE_RELATIONSHIP structure


## -description


Describes cache attributes. This structure is used with the <a href="https://docs.microsoft.com/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex">GetLogicalProcessorInformationEx</a> function.


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

The cache type. This member is a <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ne-winnt-processor_cache_type">PROCESSOR_CACHE_TYPE</a> value.


### -field Reserved

This member is reserved.


### -field GroupMask

A <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_group_affinity">GROUP_AFFINITY</a> structure that specifies a  group number and processor affinity within the group. 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_group_affinity">GROUP_AFFINITY</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex">GetLogicalProcessorInformationEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ne-winnt-processor_cache_type">PROCESSOR_CACHE_TYPE</a>



<a href="https://docs.microsoft.com/windows/win32/api/winnt/ns-winnt-system_logical_processor_information_ex">SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX</a>
 

 

