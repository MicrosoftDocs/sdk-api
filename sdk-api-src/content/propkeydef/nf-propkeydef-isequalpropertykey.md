---
UID: NF:propkeydef.IsEqualPropertyKey
title: IsEqualPropertyKey macro (propkeydef.h)
description: Compares the members of two PROPERTYKEY structures and returns whether they are equal.
helpviewer_keywords: ["IsEqualPropertyKey","IsEqualPropertyKey macro [Windows Shell]","_shell_IsEqualPropertyKey","propkeydef/IsEqualPropertyKey","shell.IsEqualPropertyKey"]
old-location: shell\IsEqualPropertyKey.htm
tech.root: shell
ms.assetid: 89218de5-95c8-440a-bde1-e4a0bc0d0549
ms.date: 07/01/2025
ms.keywords: IsEqualPropertyKey, IsEqualPropertyKey macro [Windows Shell], _shell_IsEqualPropertyKey, propkeydef/IsEqualPropertyKey, shell.IsEqualPropertyKey
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IsEqualPropertyKey
 - propkeydef/IsEqualPropertyKey
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Propkeydef.h
api_name:
 - IsEqualPropertyKey
---

# IsEqualPropertyKey macro

## -syntax

```cpp
void IsEqualPropertyKey(
    PROPERTYKEY a,
    PROPERTYKEY b
);
```


## -description

Compares the members of two <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structures and returns whether they are equal.

## -parameters

### -param a

The first <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a>.

### -param b

The second <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a>.

## -remarks

The <b>IsEqualPropertyKey</b> macro is defined as follows. 
			


```
#define IsEqualPropertyKey(a, b)   (((a).pid == (b).pid) && IsEqualIID((a).fmtid, (b).fmtid) )
```
