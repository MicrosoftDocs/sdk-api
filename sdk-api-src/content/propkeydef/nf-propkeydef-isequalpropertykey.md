---
UID: NF:propkeydef.IsEqualPropertyKey
title: IsEqualPropertyKey macro
author: windows-sdk-content
description: Compares the members of two PROPERTYKEY structures and returns whether they are equal.
old-location: shell\IsEqualPropertyKey.htm
old-project: shell
ms.assetid: 89218de5-95c8-440a-bde1-e4a0bc0d0549
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: IsEqualPropertyKey, IsEqualPropertyKey macro [Windows Shell], _shell_IsEqualPropertyKey, propkeydef/IsEqualPropertyKey, shell.IsEqualPropertyKey
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: propkeydef.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: STATPROPSTG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Propkeydef.h
api_name:
 - IsEqualPropertyKey
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IsEqualPropertyKey macro


## -description


Compares the members of two <a href="https://msdn.microsoft.com/3f5f31af-f040-443b-9045-9761055381ea">PROPERTYKEY</a> structures and returns whether they are equal.


## -parameters




### -param a

The first <a href="https://msdn.microsoft.com/3f5f31af-f040-443b-9045-9761055381ea">PROPERTYKEY</a>.


### -param b

The second <a href="https://msdn.microsoft.com/3f5f31af-f040-443b-9045-9761055381ea">PROPERTYKEY</a>.


## -remarks



The <b>IsEqualPropertyKey</b> macro is defined as follows. 
			

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>#define IsEqualPropertyKey(a, b)   (((a).pid == (b).pid) &amp;&amp; IsEqualIID((a).fmtid, (b).fmtid) )</pre>
</td>
</tr>
</table></span></div>


