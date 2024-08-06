---
UID: NF:clusapi.CLUSPROP_SZ_DECLARE
title: CLUSPROP_SZ_DECLARE macro (clusapi.h)
description: Creates a CLUSPROP_SZ structure with the sz member set to a size determined by the caller.
helpviewer_keywords: ["CLUSPROP_SZ_DECLARE","CLUSPROP_SZ_DECLARE macro [Failover Cluster]","_wolf_clusprop_sz_declare","clusapi/CLUSPROP_SZ_DECLARE","mscs.clusprop_sz_declare"]
old-location: mscs\clusprop_sz_declare.htm
tech.root: MsCS
ms.assetid: ff759673-b9cf-44fb-b4a0-4264117b24a8
ms.date: 12/05/2018
ms.keywords: CLUSPROP_SZ_DECLARE, CLUSPROP_SZ_DECLARE macro [Failover Cluster], _wolf_clusprop_sz_declare, clusapi/CLUSPROP_SZ_DECLARE, mscs.clusprop_sz_declare
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSPROP_SZ_DECLARE
 - clusapi/CLUSPROP_SZ_DECLARE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
api_name:
 - CLUSPROP_SZ_DECLARE
---

# CLUSPROP_SZ_DECLARE macro


## -description

Creates a 
    <a href="/previous-versions/windows/desktop/legacy/aa368390(v=vs.85)">CLUSPROP_SZ</a> structure with the <b>sz</b> 
    member set to a size determined by the caller.

## -parameters

### -param name

Name of the <a href="/previous-versions/windows/desktop/legacy/aa368390(v=vs.85)">CLUSPROP_SZ</a> structure to be 
      created.

### -param cch

The size (that is, count of characters) of the <b>sz</b> member array. This value must 
      be a constant.

## -remarks

ClusAPI.h defines <b>CLUSPROP_SZ_DECLARE</b> as follows:


``` syntax
#define CLUSPROP_SZ_DECLARE( name, cch )    \
    struct {                                \
        CLUSPROP_SYNTAX Syntax;             \
        DWORD           cbLength;           \
        WCHAR           sz[(cch + 1) & ~1]; \
    } name
```


#### Examples

The following example shows how to use 
     <b>CLUSPROP_SZ_DECLARE</b>:


```cpp
WCHAR szNameData[] = L"Object Name";
CLUSPROP_SZ_DECLARE( NameValue, sizeof( szNameData ) / sizeof( WCHAR ) );
NameValue.Syntax.dw = CLUSPROP_SYNTAX_LIST_VALUE_SZ;
NameValue.cbLength = sizeof( szNameData );
StringCbCopy( NameValue.sz, NameValue.cbLength, szNameData );

```

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa368390(v=vs.85)">CLUSPROP_SZ</a>
