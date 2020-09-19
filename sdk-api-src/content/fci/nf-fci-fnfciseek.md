---
UID: NF:fci.FNFCISEEK
title: FNFCISEEK macro (fci.h)
description: The FNFCISEEK macro provides the declaration for the application-defined callback function to move a file pointer to the specified location in an FCI context.
helpviewer_keywords: ["FNFCISEEK","FNFCISEEK macro [Windows API]","fci/FNFCISEEK","winprog.fnfciseek"]
old-location: winprog\fnfciseek.htm
tech.root: winprog
ms.assetid: e5a14c98-4de6-452e-8993-afb7964aeee7
ms.date: 12/05/2018
ms.keywords: FNFCISEEK, FNFCISEEK macro [Windows API], fci/FNFCISEEK, winprog.fnfciseek
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
 - FNFCISEEK
 - fci/FNFCISEEK
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
 - FNFCISEEK
---

## -description

The <b>FNFCISEEK</b> macro provides the declaration for the application-defined callback function to move a file pointer to the specified location in an FCI context.

## -parameters

### -param fn

An application-defined value used to identify the open file.

## -remarks

The function accepts parameters similar to <a href="https://msdn.microsoft.com/library/ms235323(VS.80).aspx">_lseek</a> with the addition to <i>err</i> and <i>pv</i>.

## Examples

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

<a href="/windows/desktop/api/fci/nf-fci-fcicreate">FCICreate</a>