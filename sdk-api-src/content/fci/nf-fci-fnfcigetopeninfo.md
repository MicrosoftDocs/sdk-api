---
UID: NF:fci.FNFCIGETOPENINFO
title: FNFCIGETOPENINFO macro (fci.h)
description: The FNFCIGETOPENINFO macro provides the declaration for the application-defined callback function to open a file and retrieve file date, time, and attribute.
helpviewer_keywords: ["FNFCIGETOPENINFO","FNFCIGETOPENINFO macro [Windows API]","fci/FNFCIGETOPENINFO","winprog.fnfcigetopeninfo"]
old-location: winprog\fnfcigetopeninfo.htm
tech.root: winprog
ms.assetid: 5baccb69-7872-4d67-ad74-70cdd7459f8d
ms.date: 12/05/2018
ms.keywords: FNFCIGETOPENINFO, FNFCIGETOPENINFO macro [Windows API], fci/FNFCIGETOPENINFO, winprog.fnfcigetopeninfo
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
 - FNFCIGETOPENINFO
 - fci/FNFCIGETOPENINFO
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
 - FNFCIGETOPENINFO
---

## -description

The <b>FNFCIGETOPENINFO</b> macro provides the declaration for the application-defined callback function to open a file and retrieve file date, time, and attribute.

## -parameters

### -param fn [in]

The complete filename.

## -remarks

The function should open the file using the file open function compatible with those passed into <a href="/windows/desktop/api/fci/nf-fci-fcicreate">FCICreate</a>.

## Examples

```cpp
FNFCIGETOPENINFO(fnGetOpenInfo)
{
    HANDLE hFile;
    FILETIME fileTime;
    BY_HANDLE_FILE_INFORMATION fileInfo;

    hFile = (HANDLE)fnFileOpen(pszName, _O_RDONLY, 0, err, pv);

    if ( hFile != (HANDLE)-1 )
    {
        if( GetFileInformationByHandle(hFile, &fileInfo) 
        &&  FileTimeToLocalFileTime(&fileInfo.ftCreationTime, &fileTime)
        &&  FileTimeToDosDateTime(&fileTime, pdate, ptime) )
        {
            *pattribs = (USHORT)fileInfo.dwFileAttributes;
            *pattribs &= ( _A_RDONLY | _A_HIDDEN | _A_SYSTEM | _A_ARCH );
        }
        else
        {
            fnFileClose((INT_PTR)hFile, err, pv);
            hFile = (HANDLE)-1;
        }
    }

    return (INT_PTR)hFile;
}
```

## -see-also

<a href="/windows/desktop/api/fci/nf-fci-fcicreate">FCICreate</a>
