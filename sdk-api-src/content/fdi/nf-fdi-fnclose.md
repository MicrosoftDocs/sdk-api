---
UID: NF:fdi.FNCLOSE
title: FNCLOSE macro (fdi.h)
description: The FNCLOSE macro provides the declaration for the application-defined callback function to close a file in an FDI context.
helpviewer_keywords: ["FNCLOSE","FNCLOSE macro [Windows API]","fdi/FNCLOSE","winprog.fnclose"]
old-location: winprog\fnclose.htm
tech.root: winprog
ms.assetid: 89db9c2a-42ab-410d-a427-60d282385c2b
ms.date: 12/05/2018
ms.keywords: FNCLOSE, FNCLOSE macro [Windows API], fdi/FNCLOSE, winprog.fnclose
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
 - FNCLOSE
 - fdi/FNCLOSE
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
 - FNCLOSE
---

# FNCLOSE macro


## -description

The <b>FNCLOSE</b> macro provides the declaration for the application-defined callback function to close a file in an FDI context.

## -parameters

### -param fn [in]

An application-defined value used to identify the open file.

## -remarks

The function accepts parameters similar to <a href="https://msdn.microsoft.com/library/5fzwd5ss(VS.80).aspx">_close</a>.


#### Examples


```cpp
FNCLOSE(fnFileClose)
{
    return ( CloseHandle((HANDLE)hf) == TRUE ) ? 0 : -1;
}

```

