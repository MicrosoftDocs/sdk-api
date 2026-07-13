---
UID: NF:fdi.FNOPEN
title: FNOPEN macro (fdi.h)
description: The FNOPEN macro provides the declaration for the application-defined callback function to open a file in an FDI context.
helpviewer_keywords: ["FNOPEN","FNOPEN macro [Windows API]","fdi/FNOPEN","winprog.fnopen"]
old-location: winprog\fnopen.htm
tech.root: winprog
ms.assetid: 45bd2d23-1f6d-42a6-8afb-86227da6118f
ms.date: 12/05/2018
ms.keywords: FNOPEN, FNOPEN macro [Windows API], fdi/FNOPEN, winprog.fnopen
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
 - FNOPEN
 - fdi/FNOPEN
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
 - FNOPEN
---

## -description

The <b>FNOPEN</b> macro provides the declaration for the application-defined callback function to open a file in an FDI context.

## -parameters

### -param fn [in]

The name of the file.

In the case of a file in the cabinet, the name comes directly from the cabinet file.
If the cabinet file is malicious, the name may contain illegal or malicious file name characters.

## -remarks

The function accepts parameters similar to <a href="https://msdn.microsoft.com/library/z0kc8e3z(VS.71).aspx">_open</a>.

## Examples


```cpp
FNOPEN(fnFileOpen)
{
    HANDLE hFile = NULL;
    DWORD dwDesiredAccess = 0; 
    DWORD dwCreationDisposition = 0;

    UNREFERENCED_PARAMETER(pmode);

    if ( oflag & _O_RDWR )
    {
        dwDesiredAccess = GENERIC_READ | GENERIC_WRITE;
    }
    else if ( oflag & _O_WRONLY )
    {
        dwDesiredAccess = GENERIC_WRITE;
    }
    else
    {
        dwDesiredAccess = GENERIC_READ;
    }

    if ( oflag & _O_CREAT )
    {
        dwCreationDisposition = CREATE_ALWAYS;
    }
    else
    {
        dwCreationDisposition = OPEN_EXISTING;
    }

    hFile = CreateFileA(pszFile, 
                        dwDesiredAccess,
                        FILE_SHARE_READ,
                        NULL,
                        dwCreationDisposition,
                        FILE_ATTRIBUTE_NORMAL,
                        NULL);

    return (INT_PTR)hFile;
}
```

## -see-also

<a href="/windows/desktop/api/fdi/nf-fdi-fdicreate">FDICreate</a>
