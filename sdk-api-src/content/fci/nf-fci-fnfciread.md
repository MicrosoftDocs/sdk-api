---
UID: NF:fci.FNFCIREAD
title: FNFCIREAD macro (fci.h)
description: The FNFCIREAD macro provides the declaration for the application-defined callback function to read data from a file in an FCI context.
old-location: winprog\fnfciread.htm
tech.root: DevNotes
ms.assetid: dd4e97ff-efbc-462b-b954-bc3260fa1513
ms.date: 12/05/2018
ms.keywords: FNFCIREAD, FNFCIREAD macro [Windows API], fci/FNFCIREAD, winprog.fnfciread
f1_keywords:
- fci/FNFCIREAD
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
- FNFCIREAD
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# FNFCIREAD macro


## -description


The <b>FNFCIREAD</b> macro provides the declaration for the application-defined callback function to read data from a file in an FCI context.


## -parameters




### -param fn

An application-defined value used to identify the open file.


#### - cb

The maximum number of bytes to read.


#### - err

Pointer to the error code value. This value will be used to provide extended error information in the <a href="https://docs.microsoft.com/windows/desktop/api/fdi_fci_types/ns-fdi_fci_types-erf">ERF</a> structure used to create the FCI context.


#### - memory

Pointer to the buffer that receives the data read from a file.


#### - pv

Pointer to an application-defined value


## -remarks



The function accepts parameters similar to<a href="https://go.microsoft.com/fwlink/p/?linkid=196544"> _read</a> with the addition to <i>err</i> and <i>pv</i>.


#### Examples


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




<a href="https://docs.microsoft.com/windows/desktop/api/fci/nf-fci-fcicreate">FCICreate</a>
 

 

