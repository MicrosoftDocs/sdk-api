---
UID: NF:fdi.FNFREE
title: FNFREE macro (fdi.h)
description: The FNFREE macro provides the declaration for the application-defined callback function to free previously allocated memory in an FDI context.
helpviewer_keywords: ["FNFREE","FNFREE macro [Windows API]","fdi/FNFREE","winprog.fnfree"]
old-location: winprog\fnfree.htm
tech.root: winprog
ms.assetid: 646a0cb4-1f3a-42a1-a508-12d80bdb4a01
ms.date: 12/05/2018
ms.keywords: FNFREE, FNFREE macro [Windows API], fdi/FNFREE, winprog.fnfree
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
 - FNFREE
 - fdi/FNFREE
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
 - FNFREE
---

# FNFREE macro


## -description

The <b>FNFREE</b> macro provides the declaration for the application-defined callback function to free previously allocated memory in an FDI context.

## -parameters

### -param fn [in, optional]

Pointer to the allocated memory block to free.

## -remarks

The function accepts parameters similar to <a href="https://msdn.microsoft.com/library/we1whae7(VS.80).aspx">free</a>.


#### Examples


```cpp
FNFREE(fnMemFree)
{
    free(pv);
}

```

## -see-also

<a href="/windows/desktop/api/fdi/nf-fdi-fdicreate">FDICreate</a>