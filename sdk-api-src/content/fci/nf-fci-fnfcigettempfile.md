---
UID: NF:fci.FNFCIGETTEMPFILE
title: FNFCIGETTEMPFILE macro (fci.h)
description: The FNFCIGETTEMPFILE macro provides the declaration for the application-defined callback function to obtain a temporary file name.
helpviewer_keywords: ["FNFCIGETTEMPFILE","FNFCIGETTEMPFILE macro [Windows API]","fci/FNFCIGETTEMPFILE","winprog.fnfcigettempfile"]
old-location: winprog\fnfcigettempfile.htm
tech.root: winprog
ms.assetid: 8978f688-d8f1-437a-b298-eed1e7dac012
ms.date: 12/05/2018
ms.keywords: FNFCIGETTEMPFILE, FNFCIGETTEMPFILE macro [Windows API], fci/FNFCIGETTEMPFILE, winprog.fnfcigettempfile
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
 - FNFCIGETTEMPFILE
 - fci/FNFCIGETTEMPFILE
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
 - FNFCIGETTEMPFILE
---

## -description

The <b>FNFCIGETTEMPFILE</b> macro provides the declaration for the application-defined callback function to obtain a temporary file name.

## -parameters

### -param fn [out]

Pointer to a buffer to receive the complete temporary file name.

## -remarks

The function can return a filename that already exists by the time it is opened. For this reason, the caller should be prepared to make several attempts to create temporary files.

## Examples

```cpp
FNFCIGETTEMPFILE(fnGetTempFileName)
{
    BOOL bSucceeded = FALSE;
    CHAR pszTempPath[MAX_PATH];
    CHAR pszTempFile[MAX_PATH];

    UNREFERENCED_PARAMETER(pv);
    UNREFERENCED_PARAMETER(cbTempName);

    if( GetTempPathA(MAX_PATH, pszTempPath) != 0 )
    {
        if( GetTempFileNameA(pszTempPath, "CABINET", 0, pszTempFile) != 0 )
        {
            DeleteFileA(pszTempFile);
            bSucceeded = SUCCEEDED(StringCbCopyA(pszTempName, cbTempName, pszTempFile));
        }
    }

    return bSucceeded;
}
```

## -see-also

<a href="/windows/desktop/api/fci/nf-fci-fcicreate">FCICreate</a>
