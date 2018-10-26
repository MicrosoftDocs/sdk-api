---
UID: NF:fdi.FNREAD
title: FNREAD macro
author: windows-sdk-content
description: The FNREAD macro provides the declaration for the application-defined callback function to read data from a file in an FDI context.
old-location: winprog\fnread.htm
tech.root: devnotes
ms.assetid: 0a8c6c9f-051c-43a0-b43b-1fd8b4fef10c
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: FNREAD, FNREAD macro [Windows API], fdi/FNREAD, winprog.fnread
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
 - FNREAD
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FNREAD macro


## -description


The <b>FNREAD</b> macro provides the declaration for the application-defined callback function to read data from a file in an FDI context.


## -parameters




### -param fn [in]

An application-defined value used to identify the open file.


#### - cb

The maximum number of bytes to be read.


#### - pv [out]

Pointer to the buffer that receives the data read from a file.


## -remarks



The function accepts parameters similar to<a href="http://go.microsoft.com/fwlink/p/?linkid=196544"> _read</a>.


#### Examples


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




<a href="https://msdn.microsoft.com/90634725-b7a8-4369-8a91-684debee9548">FDICreate</a>
 

 

