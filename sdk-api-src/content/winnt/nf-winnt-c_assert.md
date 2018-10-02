---
UID: NF:winnt.C_ASSERT
title: C_ASSERT macro
author: windows-sdk-content
description: Checks assertions at compile time.
old-location: base\c_assert.htm
tech.root: debug
ms.assetid: 6cae9a14-584c-474c-b34e-7c6e410afcc1
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: C_ASSERT, C_ASSERT macro, base.c_assert, winnt/C_ASSERT
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
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
 - C_ASSERT
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# C_ASSERT macro


## -description


Checks assertions at compile time.


## -parameters




### -param e

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


