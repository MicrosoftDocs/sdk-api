---
UID: NF:clusapi.CLUSPROP_SZ_DECLARE
title: CLUSPROP_SZ_DECLARE macro
author: windows-sdk-content
description: Creates a CLUSPROP_SZ structure with the sz member set to a size determined by the caller.
old-location: mscs\clusprop_sz_declare.htm
tech.root: mscs
ms.assetid: ff759673-b9cf-44fb-b4a0-4264117b24a8
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: CLUSPROP_SZ_DECLARE, CLUSPROP_SZ_DECLARE macro [Failover Cluster], _wolf_clusprop_sz_declare, clusapi/CLUSPROP_SZ_DECLARE, mscs.clusprop_sz_declare
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
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
 - ClusAPI.h
api_name:
 - CLUSPROP_SZ_DECLARE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CLUSPROP_SZ_DECLARE macro


## -description


Creates a 
    <a href="https://msdn.microsoft.com/f991ac6f-5272-44ee-a035-c9501bf7d866">CLUSPROP_SZ</a> structure with the <b>sz</b> 
    member set to a size determined by the caller.


## -parameters




### -param name

Name of the <a href="https://msdn.microsoft.com/f991ac6f-5272-44ee-a035-c9501bf7d866">CLUSPROP_SZ</a> structure to be 
      created.


### -param cch

The size (that is, count of characters) of the <b>sz</b> member array. This value must 
      be a constant.


## -remarks



ClusAPI.h defines <b>CLUSPROP_SZ_DECLARE</b> as follows:

<pre class="syntax" xml:space="preserve"><code>#define CLUSPROP_SZ_DECLARE( name, cch )    \
    struct {                                \
        CLUSPROP_SYNTAX Syntax;             \
        DWORD           cbLength;           \
        WCHAR           sz[(cch + 1) &amp; ~1]; \
    } name</code></pre>

#### Examples

The following example shows how to use 
     <b>CLUSPROP_SZ_DECLARE</b>:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>WCHAR szNameData[] = L"Object Name";
CLUSPROP_SZ_DECLARE( NameValue, sizeof( szNameData ) / sizeof( WCHAR ) );
NameValue.Syntax.dw = CLUSPROP_SYNTAX_LIST_VALUE_SZ;
NameValue.cbLength = sizeof( szNameData );
StringCbCopy( NameValue.sz, NameValue.cbLength, szNameData );
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/f991ac6f-5272-44ee-a035-c9501bf7d866">CLUSPROP_SZ</a>
 

 

