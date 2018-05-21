---
UID: NF:winnt.PreFetchCacheLine
title: PreFetchCacheLine macro
author: windows-driver-content
description: Indicates to the processor that a cache line will be needed in the near future.
old-location: base\prefetchcacheline.htm
old-project: Sync
ms.assetid: 112f3acc-e9d4-44c0-8844-1dc8cc1de2c8
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: PF_NON_TEMPORAL_LEVEL_ALL, PF_TEMPORAL_LEVEL_1, PreFetchCacheLine, PreFetchCacheLine macro, base.prefetchcacheline, winnt/PreFetchCacheLine
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TRANSACTION_OUTCOME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winnt.h
api_name:
-	PreFetchCacheLine
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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


