---
UID: NF:clusapi.CLUSPROP_PROPERTY_NAME_DECLARE
title: CLUSPROP_PROPERTY_NAME_DECLARE macro
author: windows-sdk-content
description: Creates a CLUSPROP_PROPERTY_NAME structure with the sz member set to a size determined by the caller.
old-location: mscs\clusprop_property_name_declare.htm
tech.root: mscs
ms.assetid: 8947baed-3a96-4986-94ea-4b275908acdc
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: CLUSPROP_PROPERTY_NAME_DECLARE, CLUSPROP_PROPERTY_NAME_DECLARE macro [Failover Cluster], _wolf_clusprop_property_name_declare, clusapi/CLUSPROP_PROPERTY_NAME_DECLARE, mscs.clusprop_property_name_declare
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
 - CLUSPROP_PROPERTY_NAME_DECLARE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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


```cpp
WCHAR szName[] = L"Name";
CLUSPROP_PROPERTY_NAME_DECLARE( PropName, sizeof( szName ) / sizeof( WCHAR ) );
PropName.Syntax.dw = CLUSPROP_SYNTAX_LIST_VALUE_SZ;
PropName.cbLength  = sizeof( szName );
StringCbCopy( PropName.sz, PropName.cbLength, szName );

```





## -see-also




<a href="https://msdn.microsoft.com/bb2e904c-2782-45f6-b95d-b1b107fa0060">CLUSPROP_PROPERTY_NAME</a>
 

 

