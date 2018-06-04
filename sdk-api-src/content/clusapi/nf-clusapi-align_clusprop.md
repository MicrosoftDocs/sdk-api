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

# ALIGN_CLUSPROP macro


## -description


Aligns structures properly within  <a href="https://msdn.microsoft.com/f2b20fe5-0d7e-4ccd-b288-aa8104a24fef">value lists</a>.


## -parameters




### -param count

Size, in bytes, of the data to align. This value must be a constant.


## -remarks



<b>ALIGN_CLUSPROP</b> returns a value that is greater than or equal to <i>count</i>. The value represents the total byte size of the data plus the padding required for proper alignment.

ClusAPI.h defines  <b>ALIGN_CLUSPROP</b> as follows:

<code>#define ALIGN_CLUSPROP( count ) ((count + 3) &amp; ~3)</code>


#### Examples

The following example illustrates how to use  <b>ALIGN_CLUSPROP</b> to calculate the size of a value list entry. For additional examples, see  <a href="https://msdn.microsoft.com/f8f0297a-c050-41b9-a52f-a0265a18b87a">Using Lists and Tables</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>WCHAR szData[] = L"StringData";
DWORD cbSizeofValueListEntry;

cbSizeofValueListEntry = sizeof( CLUSPROP_VALUE ) + 
                         ALIGN_CLUSPROP( sizeof( szData ) );
</pre>
</td>
</tr>
</table></span></div>


