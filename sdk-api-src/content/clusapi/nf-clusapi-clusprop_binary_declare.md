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

# CLUSPROP_BINARY_DECLARE macro


## -description


Creates a  <a href="https://msdn.microsoft.com/61169871-4998-4e9f-97dc-77344bbfa962">CLUSPROP_BINARY</a> structure with the <b>rgb</b> member set to a size determined by the caller.


## -parameters




### -param name

Name of the  <a href="https://msdn.microsoft.com/61169871-4998-4e9f-97dc-77344bbfa962">CLUSPROP_BINARY</a> structure to be created.


### -param cb

The size (count of bytes) of the <b>rgb</b> member array. This value must be a constant.


## -remarks



ClusAPI.h defines  <b>CLUSPROP_BINARY_DECLARE</b> as follows:

<pre class="syntax" xml:space="preserve"><code>#define CLUSPROP_BINARY_DECLARE( name, cch )    \
    struct {                                \
        CLUSPROP_SYNTAX Syntax;             \
        DWORD           cbLength;           \
        BYTE            rgb[(cch + 3) &amp; ~3]; \
    } name</code></pre>

#### Examples

The following example shows how to use  <b>CLUSPROP_BINARY_DECLARE</b>:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BYTE ByteData[] = { 'A', 1, 'B', 2, 'C' };
CLUSPROP_BINARY_DECLARE( ByteValue, sizeof( ByteData ) );
ByteValue.Syntax.dw = CLUSPROP_SYNTAX_LIST_VALUE_SZ;
ByteValue.cbLength = sizeof( ByteData );
memcpy( ByteValue.rgb, ByteData, sizeof( ByteData ) );
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/61169871-4998-4e9f-97dc-77344bbfa962">CLUSPROP_BINARY</a>
 

 

