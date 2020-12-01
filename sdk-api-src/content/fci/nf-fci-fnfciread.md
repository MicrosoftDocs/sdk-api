---
UID: NF:fci.FNFCIREAD
title: FNFCIREAD macro (fci.h)
description: The FNFCIREAD macro provides the declaration for the application-defined callback function to read data from a file in an FCI context.
helpviewer_keywords: ["FNFCIREAD","FNFCIREAD macro [Windows API]","fci/FNFCIREAD","winprog.fnfciread"]
old-location: winprog\fnfciread.htm
tech.root: winprog
ms.assetid: dd4e97ff-efbc-462b-b954-bc3260fa1513
ms.date: 12/05/2018
ms.keywords: FNFCIREAD, FNFCIREAD macro [Windows API], fci/FNFCIREAD, winprog.fnfciread
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
 - FNFCIREAD
 - fci/FNFCIREAD
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
 - FNFCIREAD
---

## -description

The <b>FNFCIREAD</b> macro provides the declaration for the application-defined callback function to read data from a file in an FCI context.

## -parameters

### -param fn

An application-defined value used to identify the open file.

## -remarks

The function accepts parameters similar to<a href="https://msdn.microsoft.com/library/wyssk1bs(VS.80).aspx"> _read</a> with the addition to <i>err</i> and <i>pv</i>.

## Examples

```cpp
FNFCIREAD(fnFileRead)
{
    DWORD dwBytesRead = 0;

    UNREFERENCED_PARAMETER(pv);

    if( ReadFile((HANDLE)hf, memory, cb, &dwBytesRead, NULL) == FALSE )
    {
        dwBytesRead = (DWORD)-1;
        *err = GetLastError();
    }
         
    return dwBytesRead;
}
```

## -see-also

<a href="/windows/desktop/api/fci/nf-fci-fcicreate">FCICreate</a>