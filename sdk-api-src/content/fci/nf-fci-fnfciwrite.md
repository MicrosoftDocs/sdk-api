---
UID: NF:fci.FNFCIWRITE
title: FNFCIWRITE macro (fci.h)
description: The FNFCIWRITE macro provides the declaration for the application-defined callback function to write data to a file in an FCI context.
helpviewer_keywords: ["FNFCIWRITE","FNFCIWRITE macro [Windows API]","fci/FNFCIWRITE","winprog.fnfciwrite"]
old-location: winprog\fnfciwrite.htm
tech.root: winprog
ms.assetid: ca4c3b5b-1ed5-4f12-8317-c1e1dac5f816
ms.date: 12/05/2018
ms.keywords: FNFCIWRITE, FNFCIWRITE macro [Windows API], fci/FNFCIWRITE, winprog.fnfciwrite
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
 - FNFCIWRITE
 - fci/FNFCIWRITE
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
 - FNFCIWRITE
---

## -description

The <b>FNFCIWRITE</b> macro provides the declaration for the application-defined callback function to write data to a file in an FCI context.

## -parameters

### -param fn

An application-defined value used to identify the open file.

## -remarks

The function accepts parameters similar to <a href="https://msdn.microsoft.com/library/1570wh78(VS.80).aspx">_write</a>.

## Examples

```cpp
FNFCIWRITE(fnFileWrite)
{
    DWORD dwBytesWritten = 0;

    UNREFERENCED_PARAMETER(pv);

    if ( WriteFile((HANDLE)hf, memory, cb, &dwBytesWritten, NULL) == FALSE )
    {
        dwBytesWritten = (DWORD)-1;
        *err = GetLastError();
    }

    return dwBytesWritten;
}
```

## -see-also

<a href="/windows/desktop/api/fci/nf-fci-fcicreate">FCICreate</a>