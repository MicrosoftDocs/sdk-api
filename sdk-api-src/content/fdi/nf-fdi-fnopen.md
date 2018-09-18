---
UID: NF:fdi.FNOPEN
title: FNOPEN macro
author: windows-sdk-content
description: The FNOPEN macro provides the declaration for the application-defined callback function to open a file in an FDI context.
old-location: winprog\fnopen.htm
tech.root: devnotes
ms.assetid: 45bd2d23-1f6d-42a6-8afb-86227da6118f
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: FNOPEN, FNOPEN macro [Windows API], fdi/FNOPEN, winprog.fnopen
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - fdi.h
api_name:
 - FNOPEN
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FNOPEN macro


## -description


The <b>FNOPEN</b> macro provides the declaration for the application-defined callback function to open a file in an FDI context.


## -parameters




### -param fn [in]

The name of the file.


#### - oflag

Specifies the type of operations allowed.


#### - pmode

Specifies the permission mode.


## -remarks



The function accepts parameters similar to <a href="http://go.microsoft.com/fwlink/p/?linkid=196548">_open</a>.


#### Examples


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




<a href="https://msdn.microsoft.com/90634725-b7a8-4369-8a91-684debee9548">FDICreate</a>
 

 

