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

# C_ASSERT macro


## -description


Checks assertions at compile time.


## -parameters




### -param e

TBD






#### - expr

An expression that can be determined at compile time.


## -remarks



The <b>C_ASSERT</b> macro is defined as follows.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#define C_ASSERT(e) typedef char __C_ASSERT__[(e)?1:-1]</pre>
</td>
</tr>
</table></span></div>
The following examples demonstrate common types of compile-time assertions.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>C_ASSERT (BUFFER_CCH_SIZE &lt;= MAX_PATH);

C_ASSERT (ARRAYSIZE(array1) == ARRAYSIZE(array2));

C_ASSERT (FIELD_OFFSET(STRUCT_DEF, MemberName) == 0x1d4);

C_ASSERT (sizeof(BOOLEAN) == sizeof(UCHAR));</pre>
</td>
</tr>
</table></span></div>


