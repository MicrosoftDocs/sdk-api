---
UID: NF:fci.FNFCIGETTEMPFILE
title: FNFCIGETTEMPFILE macro
author: windows-sdk-content
description: The FNFCIGETTEMPFILE macro provides the declaration for the application-defined callback function to obtain a temporary file name.
old-location: winprog\fnfcigettempfile.htm
tech.root: DevNotes
ms.assetid: 8978f688-d8f1-437a-b298-eed1e7dac012
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FNFCIGETTEMPFILE, FNFCIGETTEMPFILE macro [Windows API], fci/FNFCIGETTEMPFILE, winprog.fnfcigettempfile
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
 - FNFCIGETTEMPFILE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FNFCIGETTEMPFILE macro


## -description


The <b>FNFCIGETTEMPFILE</b> macro provides the declaration for the application-defined callback function to obtain a temporary file name.


## -parameters




### -param fn [out]

Pointer to a buffer to receive the complete temporary file name.


#### - cbTempName [in]

 Size, in bytes, of the <i>pszTempName</i> buffer.


#### - pv

Pointer to an application-defined value.


## -remarks



The function can return a filename that already exists by the time it is opened. For this reason, the caller should be prepared to make several attempts to create temporary files.


#### Examples


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




<a href="https://msdn.microsoft.com/bfcea06d-2f09-405c-955c-0f56149148f2">FCICreate</a>
 

 

