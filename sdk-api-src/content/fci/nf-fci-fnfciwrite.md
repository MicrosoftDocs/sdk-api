---
UID: NF:fci.FNFCIWRITE
title: FNFCIWRITE macro (fci.h)
description: The FNFCIWRITE macro provides the declaration for the application-defined callback function to write data to a file in an FCI context.
helpviewer_keywords: ["FNFCIWRITE","FNFCIWRITE macro [Windows API]","fci/FNFCIWRITE","winprog.fnfciwrite"]
old-location: winprog\fnfciwrite.htm
tech.root: DevNotes
ms.assetid: ca4c3b5b-1ed5-4f12-8317-c1e1dac5f816
ms.date: 12/05/2018
ms.keywords: FNFCIWRITE, FNFCIWRITE macro [Windows API], fci/FNFCIWRITE, winprog.fnfciwrite
f1_keywords:
- fci/FNFCIWRITE
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
- FNFCIWRITE
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# FNFCIWRITE macro


## -description


The <b>FNFCIWRITE</b> macro provides the declaration for the application-defined callback function to write data to a file in an FCI context.


## -parameters




### -param fn

An application-defined value used to identify the open file.


#### - cb

The maximum number of bytes to be written.


#### - err

Pointer to the error code value. This value is used when providing extended error information in the <a href="https://docs.microsoft.com/windows/desktop/api/fdi_fci_types/ns-fdi_fci_types-erf">ERF</a> structure used to create the FCI context.


#### - memory

Pointer to the buffer containing the data to be written.


#### - pv

Pointer to an application-defined value.


## -remarks



The function accepts parameters similar to <a href="https://msdn.microsoft.com/library/1570wh78(VS.80).aspx">_write</a>.


#### Examples


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




<a href="https://docs.microsoft.com/windows/desktop/api/fci/nf-fci-fcicreate">FCICreate</a>
 

 

