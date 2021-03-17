---
UID: NF:fdi.FNALLOC
title: FNALLOC macro (fdi.h)
description: The FNALLOC provides the declaration for the application-defined callback function to allocate memory in an FDI context.
helpviewer_keywords: ["FNALLOC","FNALLOC macro [Windows API]","fdi/FNALLOC","winprog.fnalloc"]
old-location: winprog\fnalloc.htm
tech.root: winprog
ms.assetid: 3104267d-3efd-40da-a8b6-af2acf379ff8
ms.date: 12/05/2018
ms.keywords: FNALLOC, FNALLOC macro [Windows API], fdi/FNALLOC, winprog.fnalloc
req.header: fdi.h
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
 - FNALLOC
 - fdi/FNALLOC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - fdi.h
api_name:
 - FNALLOC
---

# FNALLOC macro


## -description

The <b>FNALLOC</b> provides the declaration for the application-defined callback function to allocate memory in an FDI context.

## -parameters

### -param fn

The number of bytes to allocate.

## -remarks

The function accepts parameters similar to <a href="https://msdn.microsoft.com/library/6ewkz86d(VS.80).aspx">malloc</a>.


#### Examples


```cpp
FNALLOC(fnMemAlloc)
{
    return malloc(cb);
}

```

## -see-also

<a href="/windows/desktop/api/fdi/nf-fdi-fnfree">FNFree</a>