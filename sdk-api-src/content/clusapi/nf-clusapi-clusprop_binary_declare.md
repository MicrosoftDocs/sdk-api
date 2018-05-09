---
UID: NF:clusapi.CLUSPROP_BINARY_DECLARE
title: CLUSPROP_BINARY_DECLARE macro
author: windows-driver-content
description: Creates a CLUSPROP_BINARY structure with the rgb member set to a size determined by the caller.
old-location: mscs\clusprop_binary_declare.htm
old-project: MsCS
ms.assetid: f4730126-9dbf-438a-a9f2-9e917e5888b8
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: CLUSPROP_BINARY_DECLARE, CLUSPROP_BINARY_DECLARE macro [Failover Cluster], _wolf_clusprop_binary_declare, clusapi/CLUSPROP_BINARY_DECLARE, mscs.clusprop_binary_declare
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
req.typenames: SR_REPLICATED_DISK_TYPE, *PSR_REPLICATED_DISK_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ClusAPI.h
api_name:
-	CLUSPROP_BINARY_DECLARE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

