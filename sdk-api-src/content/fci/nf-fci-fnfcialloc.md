---
UID: NF:fci.FNFCIALLOC
title: FNFCIALLOC macro (fci.h)
description: The FNFCIALLOC provides the declaration for the application-defined callback function to allocate memory within an FCI context.
helpviewer_keywords: ["FNFCIALLOC","FNFCIALLOC macro [Windows API]","fci/FNFCIALLOC","winprog.fnfcialloc"]
old-location: winprog\fnfcialloc.htm
tech.root: winprog
ms.assetid: 339ac9d2-60bc-4a90-8a46-6fbb073be9d1
ms.date: 12/05/2018
ms.keywords: FNFCIALLOC, FNFCIALLOC macro [Windows API], fci/FNFCIALLOC, winprog.fnfcialloc
req.header: fci.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - FNFCIALLOC
 - fci/FNFCIALLOC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - fci.h
api_name:
 - FNFCIALLOC
---

# FNFCIALLOC macro


## -description

The <b>FNFCIALLOC</b> provides the declaration for the application-defined callback function to allocate memory within an FCI context.

## -parameters

### -param fn

The number of bytes to allocate.

## -remarks

The function accepts parameters similar to <a href="https://msdn.microsoft.com/library/6ewkz86d(VS.80).aspx">malloc</a>.


#### Examples


```cpp
FNFCIALLOC(fnMemAlloc)
{
    return malloc(cb);
}

```

## -see-also

<a href="/windows/desktop/api/fci/nf-fci-fcicreate">FCICreate</a>