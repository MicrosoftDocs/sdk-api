---
UID: NF:fci.FNFCICLOSE
title: FNFCICLOSE macro (fci.h)
description: The FNFCICLOSE macro provides the declaration for the application-defined callback function to close a file in an FCI context.
old-location: winprog\fnfciclose.htm
tech.root: DevNotes
ms.assetid: c4edf6ca-0b16-4e30-933b-934f8930c6d6
ms.date: 12/05/2018
ms.keywords: FNFCICLOSE, FNFCICLOSE macro [Windows API], fci/FNFCICLOSE, winprog.fnfciclose
f1_keywords:
- fci/FNFCICLOSE
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
- FNFCICLOSE
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# FNFCICLOSE macro


## -description


The <b>FNFCICLOSE</b> macro provides the declaration for the application-defined callback function to close a file in an FCI context.


## -parameters




### -param fn

 Specifies an application-defined value that identifies an open file.


#### - err

Pointer to the error code value. This value is  used to provide extended error information in the <a href="https://docs.microsoft.com/windows/desktop/api/fdi_fci_types/ns-fdi_fci_types-erf">ERF</a> structure used to create the FCI context.


#### - pv

Pointer to an application-defined value.


## -remarks



The function accepts parameters similar to <a href="http://go.microsoft.com/fwlink/p/?linkid=196541">_close</a>, with the addition of <i>err</i> and <i>pv</i>.


#### Examples


```cpp
FNFCICLOSE(fnFileClose)
{
    INT iResult = 0; 

    UNREFERENCED_PARAMETER(pv);
    
    if ( CloseHandle((HANDLE)hf) == FALSE)
    {
        *err = GetLastError();
        iResult = -1;
    }

    return iResult;
}

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/fci/nf-fci-fcicreate">FCICreate</a>
 

 

