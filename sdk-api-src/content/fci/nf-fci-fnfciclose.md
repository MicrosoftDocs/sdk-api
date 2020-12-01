---
UID: NF:fci.FNFCICLOSE
title: FNFCICLOSE macro (fci.h)
description: The FNFCICLOSE macro provides the declaration for the application-defined callback function to close a file in an FCI context.
helpviewer_keywords: ["FNFCICLOSE","FNFCICLOSE macro [Windows API]","fci/FNFCICLOSE","winprog.fnfciclose"]
old-location: winprog\fnfciclose.htm
tech.root: winprog
ms.assetid: c4edf6ca-0b16-4e30-933b-934f8930c6d6
ms.date: 12/05/2018
ms.keywords: FNFCICLOSE, FNFCICLOSE macro [Windows API], fci/FNFCICLOSE, winprog.fnfciclose
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
 - FNFCICLOSE
 - fci/FNFCICLOSE
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
 - FNFCICLOSE
---

## -description

The <b>FNFCICLOSE</b> macro provides the declaration for the application-defined callback function to close a file in an FCI context.

## -parameters

### -param fn

Specifies an application-defined value that identifies an open file.

## -remarks

The function accepts parameters similar to <a href="https://msdn.microsoft.com/library/5fzwd5ss(VS.80).aspx">_close</a>, with the addition of <i>err</i> and <i>pv</i>.

## Examples

```cpp
FNFCICLOSE(fnFileClose)
{
    INT iResult = 0; 

    UNREFERENCED_PARAMETER(pv);
    
    if ( CloseHandle((HANDLE)hf) == FALSE)
    {
        *err = GetLastError();
        iResult = -1;
    }

    return iResult;
}
```

## -see-also

<a href="/windows/desktop/api/fci/nf-fci-fcicreate">FCICreate</a>
