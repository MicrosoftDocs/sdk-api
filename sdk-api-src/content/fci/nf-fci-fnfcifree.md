---
UID: NF:fci.FNFCIFREE
title: FNFCIFREE macro (fci.h)
description: The FNFCIFREE macro provides the declaration for the application-defined callback function to free previously allocated memory in an FCI context.
helpviewer_keywords: ["FNFCIFREE","FNFCIFREE macro [Windows API]","fci/FNFCIFREE","winprog.fnfcifree"]
old-location: winprog\fnfcifree.htm
tech.root: winprog
ms.assetid: 48f052e2-7786-430a-b3dc-afcfdffae387
ms.date: 12/05/2018
ms.keywords: FNFCIFREE, FNFCIFREE macro [Windows API], fci/FNFCIFREE, winprog.fnfcifree
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
 - FNFCIFREE
 - fci/FNFCIFREE
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
 - FNFCIFREE
---

# FNFCIFREE macro


## -description

The <b>FNFCIFREE</b> macro provides the declaration for the application-defined callback function to free previously allocated memory in an FCI context.

## -parameters

### -param fn

Pointer to the allocated memory block to free.

## -remarks

The function accepts parameters similar to <a href="https://msdn.microsoft.com/library/we1whae7(VS.80).aspx">free</a>.


#### Examples


```cpp
FNFCIFREE(fnMemFree)
{
    free(memory);
}

```

## -see-also

<a href="/windows/desktop/api/fci/nf-fci-fcicreate">FCICreate</a>