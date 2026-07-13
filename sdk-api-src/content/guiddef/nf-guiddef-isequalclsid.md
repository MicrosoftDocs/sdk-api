---
UID: NF:guiddef.IsEqualCLSID
title: IsEqualCLSID
description: Evaluates to a Boolean value that indicates whether two CLSIDs are equal.
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
 - IsEqualCLSID
f1_keywords:
 - IsEqualCLSID
 - guiddef/IsEqualCLSID
dev_langs:
 - c++
helpviewer_keywords:
 - IsEqualCLSID
---

## -description

Evaluates to a Boolean value that indicates whether two CLSIDs are equal.

## -syntax

```cpp
BOOL IsEqualCLSID(
  rclsid1,
  rclsid2
);
```

## -parameters

### -param rclsid1

The first CLSID.

### -param rclsid2

The second CLSID.

## -returns

`TRUE` if the two CLSIDs are equal; otherwise, `FALSE`.

## -remarks

## -see-also
