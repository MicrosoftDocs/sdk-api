---
UID: NF:fci.FNFCISEEK
title: FNFCISEEK macro (fci.h)
author: windows-sdk-content
description: The FNFCISEEK macro provides the declaration for the application-defined callback function to move a file pointer to the specified location in an FCI context.
old-location: winprog\fnfciseek.htm
tech.root: DevNotes
ms.assetid: e5a14c98-4de6-452e-8993-afb7964aeee7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FNFCISEEK, FNFCISEEK macro [Windows API], fci/FNFCISEEK, winprog.fnfciseek
ms.topic: macro
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
 - FNFCISEEK
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FNFCISEEK macro


## -description


The <b>FNFCISEEK</b> macro provides the declaration for the application-defined callback function to move a file pointer to the specified location in an FCI context.


## -parameters




### -param fn

An application-defined value used to identify the open file.


#### - dist

The number of bytes to move the file pointer.


#### - err

Pointer to the error code value. This value will be used to provide extended error information in the <a href="https://msdn.microsoft.com/ddbccad9-a68c-4be7-90dc-e3dd25f5cf3b">ERF</a> structure used to create the FCI context.


#### - pv

Pointer to an application-defined value.


#### - seektype

The starting point for the file pointer to move.


## -remarks



The function accepts parameters similar to <a href="http://go.microsoft.com/fwlink/p/?linkid=196546">_lseek</a> with the addition to <i>err</i> and <i>pv</i>.


#### Examples


```cpp
FNFCISEEK(fnFileSeek)
{
    INT iResult = 0;

    UNREFERENCED_PARAMETER(pv);

    iResult = SetFilePointer((HANDLE)hf, dist, NULL, seektype);

    if ( iResult == -1 )
    {
        *err = GetLastError();
    }

    return iResult;
}

```





## -see-also




<a href="https://msdn.microsoft.com/bfcea06d-2f09-405c-955c-0f56149148f2">FCICreate</a>
 

 

