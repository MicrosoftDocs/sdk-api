---
UID: NF:adshlp.ReallocADsMem
title: ReallocADsMem function (adshlp.h)
description: Reallocates and copies an existing memory block.
helpviewer_keywords: ["ReallocADsMem","ReallocADsMem function [ADSI]","_ds_reallocadsmem","adshlp/ReallocADsMem","adsi.reallocadsmem"]
old-location: adsi\reallocadsmem.htm
tech.root: adsi
ms.assetid: 471b8ae7-d3b6-4dd9-aa00-6e1d3ab278a9
ms.date: 12/05/2018
ms.keywords: ReallocADsMem, ReallocADsMem function [ADSI], _ds_reallocadsmem, adshlp/ReallocADsMem, adsi.reallocadsmem
req.header: adshlp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Activeds.lib
req.dll: Activeds.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ReallocADsMem
 - adshlp/ReallocADsMem
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Activeds.dll
api_name:
 - ReallocADsMem
---

# ReallocADsMem function


## -description

The <b>ReallocADsMem</b> function reallocates and copies an existing memory block.

## -parameters

### -param pOldMem [in]

Type: <b>LPVOID</b>

Pointer to the memory to copy. <b>ReallocADsMem</b> will free this memory with <a href="/windows/desktop/api/adshlp/nf-adshlp-freeadsmem">FreeADsMem</a> after it has been copied. If additional memory cannot be allocated, this memory is not freed. This memory must have been allocated with the <a href="/windows/desktop/api/adshlp/nf-adshlp-allocadsmem">AllocADsMem</a>, <a href="/windows/desktop/api/adshlp/nf-adshlp-allocadsstr">AllocADsStr</a>, <b>ReallocADsMem</b>, or <a href="/windows/desktop/api/adshlp/nf-adshlp-reallocadsstr">ReallocADsStr</a> function.

The caller must  free this memory when it is no longer required by passing this pointer to <a href="/windows/desktop/api/adshlp/nf-adshlp-freeadsmem">FreeADsMem</a>.

### -param cbOld [in]

Type: <b>DWORD</b>

Size, in bytes, of the memory to copy.

### -param cbNew [in]

Type: <b>DWORD</b>

Size, in bytes, of the memory to allocate.

## -returns

Type: <b>LPVOID</b>

When successful, the function returns a pointer to the new allocated memory. Otherwise it returns <b>NULL</b>.

## -remarks

If <i>cbNew</i> is less than <i>cbOld</i>, the existing memory is truncated to fit the new memory size.


#### Examples

The following code example shows how to use <b>ReallocADsMem</b> to enlarge a string.


```cpp
LPWSTR pwszPrefix = L"LDAP://"
DWORD dwOldSize = (lstrlenW(pwszPrefix) + 1) * sizeof(WCHAR);

LPWSTR pwszADsPath = (LPWSTR)AllocADsMem(dwOldSize);
if(pwszADsPath)
{
    LPWSTR pwszDN = L"DC=fabrikam,DC=com";

    wcsncpy_s(pwszADsPath, pwszPrefix); // Path becomes "LDAP://"
    wprintf(L"path = %s\n", pwszADsPath);

    DWORD dwNewSize = (lstrlenW(pwszPrefix) + lstrlenW(pwszDN) + 1) * sizeof(WCHAR);
    
    /*
    If successful, this will free the old path buffer, so it does not have to be 
    freed manually. But if it fails, the original memory still exists, so the 
    reallocated memory pointer is temporarily placed in another variable.
    */
    LPWSTR pwszNewPath = (LPWSTR)ReallocADsMem(pwszADsPath, dwOldSize, dwNewSize);
    if(pwszNewPath)
    {
        pwszADsPath = pwszNewPath;

        // Path is still "LDAP://"
        wcsncat_s(pwszADsPath, pwszDN);

        // Path is "LDAP://DC=fabrikam,DC=com"
        wprintf(L"path = %s\n", pwszADsPath);
    }
    else
    {
        wprintf(L"Unable to allocate additional memory.");
    }

    // Free remaining memory.
    FreeADsMem(pwszADsPath);
}
```

## -see-also

<a href="/windows/desktop/ADSI/adsi-functions">ADSI Functions</a>



<a href="/windows/desktop/api/adshlp/nf-adshlp-allocadsmem">AllocADsMem</a>



<a href="/windows/desktop/api/adshlp/nf-adshlp-allocadsstr">AllocADsStr</a>



<a href="/windows/desktop/api/adshlp/nf-adshlp-freeadsmem">FreeADsMem</a>



<a href="/windows/desktop/api/adshlp/nf-adshlp-reallocadsmem">ReallocADsMem</a>