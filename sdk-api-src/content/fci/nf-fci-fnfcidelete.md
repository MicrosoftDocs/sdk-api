---
UID: NF:fci.FNFCIDELETE
title: FNFCIDELETE macro (fci.h)
description: The FNFCIDELETE macro provides the declaration for the application-defined callback function to delete a file in the FCI context.
helpviewer_keywords: ["FNFCIDELETE","FNFCIDELETE macro [Windows API]","fci/FNFCIDELETE","winprog.fnfcidelete"]
old-location: winprog\fnfcidelete.htm
tech.root: winprog
ms.assetid: 5c85ad86-2794-4f7c-8c10-18fea3519b11
ms.date: 12/05/2018
ms.keywords: FNFCIDELETE, FNFCIDELETE macro [Windows API], fci/FNFCIDELETE, winprog.fnfcidelete
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
 - FNFCIDELETE
 - fci/FNFCIDELETE
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
 - FNFCIDELETE
---

## -description

The <b>FNFCIDELETE</b> macro provides the declaration for the application-defined callback function to delete a file in the FCI context.

## -parameters

### -param fn [in]

The name of the file to be deleted.

## -remarks

The function accepts parameters similar to <a href="https://msdn.microsoft.com/library/2da4hk1d(VS.80).aspx">remove</a>, with the addition of <i>err</i> and <i>pv</i>.


## Examples


```cpp
FNFCIDELETE(fnFileDelete)
{
    INT iResult = 0;

    UNREFERENCED_PARAMETER(pv);

    if ( DeleteFileA(pszFile) == FALSE)
    {
        *err = GetLastError();
        iResult = -1;
    }

    return iResult;
}


```

## -see-also

<a href="/windows/desktop/api/fci/nf-fci-fcicreate">FCICreate</a>