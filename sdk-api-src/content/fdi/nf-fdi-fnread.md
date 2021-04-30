---
UID: NF:fdi.FNREAD
title: FNREAD macro (fdi.h)
description: The FNREAD macro provides the declaration for the application-defined callback function to read data from a file in an FDI context.
helpviewer_keywords: ["FNREAD","FNREAD macro [Windows API]","fdi/FNREAD","winprog.fnread"]
old-location: winprog\fnread.htm
tech.root: winprog
ms.assetid: 0a8c6c9f-051c-43a0-b43b-1fd8b4fef10c
ms.date: 12/05/2018
ms.keywords: FNREAD, FNREAD macro [Windows API], fdi/FNREAD, winprog.fnread
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
 - FNREAD
 - fdi/FNREAD
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
 - FNREAD
---

## -description

The <b>FNREAD</b> macro provides the declaration for the application-defined callback function to read data from a file in an FDI context.

## -parameters

### -param fn [in]

An application-defined value used to identify the open file.

## -remarks

The function accepts parameters similar to<a href="https://msdn.microsoft.com/library/wyssk1bs(VS.80).aspx"> _read</a>.

## Examples

```cpp
FNREAD(fnFileRead)
{
    DWORD dwBytesRead = 0;

    if ( ReadFile((HANDLE)hf, pv, cb, &dwBytesRead, NULL) == FALSE )
    {
        dwBytesRead = (DWORD)-1L;
    }
             
    return dwBytesRead;
}
```

## -see-also

<a href="/windows/desktop/api/fdi/nf-fdi-fdicreate">FDICreate</a>
