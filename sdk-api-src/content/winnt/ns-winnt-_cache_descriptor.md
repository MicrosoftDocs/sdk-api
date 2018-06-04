---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

