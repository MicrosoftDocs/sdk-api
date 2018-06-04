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

# PreFetchCacheLine macro


## -description


Indicates to the processor that a cache line will be needed in the near future.


## -parameters




### -param l

TBD


### -param a

TBD






#### - Address

The address of the cache line to be loaded. This address is not required to be on a cache line boundary.


#### - Level

How often the cache line will be needed. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PF_TEMPORAL_LEVEL_1"></a><a id="pf_temporal_level_1"></a><dl>
<dt><b>PF_TEMPORAL_LEVEL_1</b></dt>
</dl>
</td>
<td width="60%">
The cache line should be loaded into all caches and is likely to be accessed multiple times.

</td>
</tr>
<tr>
<td width="40%"><a id="PF_NON_TEMPORAL_LEVEL_ALL"></a><a id="pf_non_temporal_level_all"></a><dl>
<dt><b>PF_NON_TEMPORAL_LEVEL_ALL</b></dt>
</dl>
</td>
<td width="60%">
The cache line is not likely to be needed again after the first reference.

</td>
</tr>
</table>
 


## -remarks



This macro can be called on all processor platforms where Windows is supported, but it  has no effect on some platforms.  The definition varies from platform to platform.  The following are some definitions of this macro in Winnt.h:

<pre class="syntax" xml:space="preserve"><code>#define PreFetchCacheLine(l, a)  _mm_prefetch((CHAR CONST *) a, l)

#define PreFetchCacheLine(l, a)

#define PreFetchCacheLine  __lfetch
</code></pre>


