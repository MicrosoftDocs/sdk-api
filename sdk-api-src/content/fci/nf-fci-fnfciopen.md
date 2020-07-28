---
UID: NF:fci.FNFCIOPEN
title: FNFCIOPEN macro (fci.h)
description: The FNFCIOPEN macro provides the declaration for the application-defined callback function to open a file in an FCI context.
helpviewer_keywords: ["FNFCIOPEN","FNFCIOPEN macro [Windows API]","fci/FNFCIOPEN","winprog.fnfciopen"]
old-location: winprog\fnfciopen.htm
tech.root: winprog
ms.assetid: 72cf50cb-c895-4953-9c4d-f8ddaa294f2a
ms.date: 12/05/2018
ms.keywords: FNFCIOPEN, FNFCIOPEN macro [Windows API], fci/FNFCIOPEN, winprog.fnfciopen
f1_keywords:
- fci/FNFCIOPEN
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- fci.h
api_name:
- FNFCIOPEN
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# FNFCIOPEN macro


## -description


The <b>FNFCIOPEN</b> macro provides the declaration for the application-defined callback function to open a file in an FCI context.


## -parameters




### -param fn [in]

The name of the file.


#### - err

Pointer to the error code value. 

This value will be used to provide extended error information in the <a href="https://docs.microsoft.com/windows/desktop/api/fdi_fci_types/ns-fdi_fci_types-erf">ERF</a> structure used to create the FCI context.


#### - oflag

Specifies the type of operations allowed.


#### - pmode

Specifies the permission mode.


#### - pv

Pointer to an application-defined value.


## -remarks



The function accepts parameters similar to <a href="https://msdn.microsoft.com/library/z0kc8e3z(VS.71).aspx">_open</a>.


#### Examples


```cpp
FNFCIOPEN(fnFileOpen)
{
    HANDLE hFile = NULL;
    DWORD dwDesiredAccess = 0; 
    DWORD dwCreationDisposition = 0;

    UNREFERENCED_PARAMETER(pv);
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

    if ( hFile == INVALID_HANDLE_VALUE )
    {
        *err = GetLastError();
    }

    return (INT_PTR)hFile;
}

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/fci/nf-fci-fcicreate">FCICreate</a>
 

 

