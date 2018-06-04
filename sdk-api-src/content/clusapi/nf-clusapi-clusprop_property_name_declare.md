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

# CLUSPROP_PROPERTY_NAME_DECLARE macro


## -description


Creates a <a href="https://msdn.microsoft.com/bb2e904c-2782-45f6-b95d-b1b107fa0060">CLUSPROP_PROPERTY_NAME</a> structure with 
    the <b>sz</b> member set to a size determined by the caller.


## -parameters




### -param name

Name of the <a href="https://msdn.microsoft.com/bb2e904c-2782-45f6-b95d-b1b107fa0060">CLUSPROP_PROPERTY_NAME</a> 
      structure to be created.


### -param cch

The size (that is, count of characters) of the <b>sz</b> member array. This value must 
      be a constant.


## -remarks



ClusAPI.h defines 
    <b>CLUSPROP_PROPERTY_NAME_DECLARE</b> as follows:

<pre class="syntax" xml:space="preserve"><code>#define CLUSPROP_PROPERTY_NAME_DECLARE( name, cch ) \
    struct {                                        \
        CLUSPROP_SYNTAX Syntax;                     \
        DWORD           cbLength;                   \
        WCHAR           sz[(cch + 1) &amp; ~1];         \
    } name</code></pre>

#### Examples

The following example shows how to use 
     <b>CLUSPROP_PROPERTY_NAME_DECLARE</b>. For 
     another example, see 
     <a href="https://msdn.microsoft.com/003bc879-d526-4f7d-8f58-a9002f78819d">Creating Physical Disk Resources</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>WCHAR szName[] = L"Name";
CLUSPROP_PROPERTY_NAME_DECLARE( PropName, sizeof( szName ) / sizeof( WCHAR ) );
PropName.Syntax.dw = CLUSPROP_SYNTAX_LIST_VALUE_SZ;
PropName.cbLength  = sizeof( szName );
StringCbCopy( PropName.sz, PropName.cbLength, szName );
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/bb2e904c-2782-45f6-b95d-b1b107fa0060">CLUSPROP_PROPERTY_NAME</a>
 

 

