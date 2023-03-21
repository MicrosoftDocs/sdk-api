---
UID: NF:guiddef.IsEqualGUID
title: IsEqualGUID
description: Evaluates to a Boolean value that indicates whether two GUIDs are equal.
tech.root: com
ms.date: 06/06/2022
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Ole32.dll
req.header: guiddef.h
req.idl: 
req.include-header: GuidDef.h, Objbase.h
req.irql: 
req.kmdf-ver: 
req.lib: Ole32.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.target-type: Windows
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - guiddef.h
api_name:
 - IsEqualGUID
f1_keywords:
 - IsEqualGUID
 - guiddef/IsEqualGUID
dev_langs:
 - c++
helpviewer_keywords:
 - IsEqualGUID
---

## -description

Evaluates to a Boolean value that indicates whether two GUIDs are equal.

## -syntax

```cpp
BOOL IsEqualGUID(
  rguid1,
  rguid2
);
```

## -parameters

### -param rguid1

The first GUID.

### -param rguid2

The second GUID.

## -returns

`TRUE` if the two GUIDs are equal; otherwise, `FALSE`.

## -remarks

**IsEqualGUID** is used by the [IsEqualCLSID](/windows/win32/api/guiddef/nf-guiddef-isequalclsid) and [IsEqualIID](/windows/win32/api/guiddef/nf-guiddef-isequaliid) macros.

## -see-also

* [IsEqualCLSID](/windows/win32/api/guiddef/nf-guiddef-isequalclsid)
* [IsEqualIID](/windows/win32/api/guiddef/nf-guiddef-isequaliid)
