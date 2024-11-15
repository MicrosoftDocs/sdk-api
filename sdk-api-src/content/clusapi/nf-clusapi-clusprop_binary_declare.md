---
UID: NF:clusapi.CLUSPROP_BINARY_DECLARE
title: CLUSPROP_BINARY_DECLARE macro (clusapi.h)
description: Creates a CLUSPROP_BINARY structure with the rgb member set to a size determined by the caller.
helpviewer_keywords: ["CLUSPROP_BINARY_DECLARE","CLUSPROP_BINARY_DECLARE macro [Failover Cluster]","_wolf_clusprop_binary_declare","clusapi/CLUSPROP_BINARY_DECLARE","mscs.clusprop_binary_declare"]
old-location: mscs\clusprop_binary_declare.htm
tech.root: MsCS
ms.assetid: f4730126-9dbf-438a-a9f2-9e917e5888b8
ms.date: 12/05/2018
ms.keywords: CLUSPROP_BINARY_DECLARE, CLUSPROP_BINARY_DECLARE macro [Failover Cluster], _wolf_clusprop_binary_declare, clusapi/CLUSPROP_BINARY_DECLARE, mscs.clusprop_binary_declare
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
 - CLUSPROP_BINARY_DECLARE
 - clusapi/CLUSPROP_BINARY_DECLARE
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
 - CLUSPROP_BINARY_DECLARE
---

# CLUSPROP_BINARY_DECLARE macro


## -description

Creates a  <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_binary">CLUSPROP_BINARY</a> structure with the <b>rgb</b> member set to a size determined by the caller.

## -parameters

### -param name

Name of the  <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_binary">CLUSPROP_BINARY</a> structure to be created.

### -param cb

The size (count of bytes) of the <b>rgb</b> member array. This value must be a constant.

## -remarks

ClusAPI.h defines  <b>CLUSPROP_BINARY_DECLARE</b> as follows:


``` syntax
#define CLUSPROP_BINARY_DECLARE( name, cch ) \
    struct {                                 \
        CLUSPROP_SYNTAX Syntax;              \
        DWORD           cbLength;            \
        BYTE            rgb[(cch + 3) & ~3]; \
    } name
```


#### Examples

The following example shows how to use  <b>CLUSPROP_BINARY_DECLARE</b>:


```cpp
BYTE ByteData[] = { 'A', 1, 'B', 2, 'C' };
CLUSPROP_BINARY_DECLARE( ByteValue, sizeof( ByteData ) );
ByteValue.Syntax.dw = CLUSPROP_SYNTAX_LIST_VALUE_SZ;
ByteValue.cbLength = sizeof( ByteData );
memcpy( ByteValue.rgb, ByteData, sizeof( ByteData ) );

```

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_binary">CLUSPROP_BINARY</a>
