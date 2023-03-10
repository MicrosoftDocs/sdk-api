---
UID: NF:guiddef.IsEqualIID
title: IsEqualIID
description: Evaluates to a Boolean value that indicates whether two IIDs are equal.
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
 - IsEqualIID
f1_keywords:
 - IsEqualIID
 - guiddef/IsEqualIID
dev_langs:
 - c++
helpviewer_keywords:
 - IsEqualIID
---

## -description

Evaluates to a Boolean value that indicates whether two IIDs are equal.

## -syntax

```cpp
BOOL IsEqualIID(
  riid1,
  riid2
);
```

## -parameters

### -param riid1

The first IID.

### -param riid2

The second IID.

## -returns

`TRUE` if the two IIDs are equal; otherwise, `FALSE`.

## -remarks

## -see-also
