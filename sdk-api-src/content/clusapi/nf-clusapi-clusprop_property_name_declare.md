---
UID: NF:clusapi.CLUSPROP_PROPERTY_NAME_DECLARE
title: CLUSPROP_PROPERTY_NAME_DECLARE macro (clusapi.h)
description: Creates a CLUSPROP_PROPERTY_NAME structure with the sz member set to a size determined by the caller.
helpviewer_keywords: ["CLUSPROP_PROPERTY_NAME_DECLARE","CLUSPROP_PROPERTY_NAME_DECLARE macro [Failover Cluster]","_wolf_clusprop_property_name_declare","clusapi/CLUSPROP_PROPERTY_NAME_DECLARE","mscs.clusprop_property_name_declare"]
old-location: mscs\clusprop_property_name_declare.htm
tech.root: MsCS
ms.assetid: 8947baed-3a96-4986-94ea-4b275908acdc
ms.date: 12/05/2018
ms.keywords: CLUSPROP_PROPERTY_NAME_DECLARE, CLUSPROP_PROPERTY_NAME_DECLARE macro [Failover Cluster], _wolf_clusprop_property_name_declare, clusapi/CLUSPROP_PROPERTY_NAME_DECLARE, mscs.clusprop_property_name_declare
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
 - CLUSPROP_PROPERTY_NAME_DECLARE
 - clusapi/CLUSPROP_PROPERTY_NAME_DECLARE
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
 - CLUSPROP_PROPERTY_NAME_DECLARE
---

# CLUSPROP_PROPERTY_NAME_DECLARE macro


## -description

Creates a <a href="/previous-versions/windows/desktop/legacy/aa368382(v=vs.85)">CLUSPROP_PROPERTY_NAME</a> structure with 
    the <b>sz</b> member set to a size determined by the caller.

## -parameters

### -param name

Name of the <a href="/previous-versions/windows/desktop/legacy/aa368382(v=vs.85)">CLUSPROP_PROPERTY_NAME</a> 
      structure to be created.

### -param cch

The size (that is, count of characters) of the <b>sz</b> member array. This value must 
      be a constant.

## -remarks

ClusAPI.h defines 
    <b>CLUSPROP_PROPERTY_NAME_DECLARE</b> as follows:


``` syntax
#define CLUSPROP_PROPERTY_NAME_DECLARE( name, cch ) \
    struct {                                        \
        CLUSPROP_SYNTAX Syntax;                     \
        DWORD           cbLength;                   \
        WCHAR           sz[(cch + 1) & ~1];         \
    } name
```


#### Examples

The following example shows how to use 
     <b>CLUSPROP_PROPERTY_NAME_DECLARE</b>. For 
     another example, see 
     <a href="/previous-versions/windows/desktop/mscs/creating-physical-disk-resources">Creating Physical Disk Resources</a>.


```cpp
WCHAR szName[] = L"Name";
CLUSPROP_PROPERTY_NAME_DECLARE( PropName, sizeof( szName ) / sizeof( WCHAR ) );
PropName.Syntax.dw = CLUSPROP_SYNTAX_LIST_VALUE_SZ;
PropName.cbLength  = sizeof( szName );
StringCbCopy( PropName.sz, PropName.cbLength, szName );

```

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa368382(v=vs.85)">CLUSPROP_PROPERTY_NAME</a>
