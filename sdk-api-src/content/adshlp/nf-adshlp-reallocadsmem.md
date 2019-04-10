---
UID: NF:adshlp.ReallocADsMem
title: ReallocADsMem function (adshlp.h)
author: windows-sdk-content
description: Reallocates and copies an existing memory block.
old-location: adsi\reallocadsmem.htm
tech.root: adsi
ms.assetid: 471b8ae7-d3b6-4dd9-aa00-6e1d3ab278a9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ReallocADsMem, ReallocADsMem function [ADSI], _ds_reallocadsmem, adshlp/ReallocADsMem, adsi.reallocadsmem
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Activeds.dll
api_name:
 - ReallocADsMem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ReallocADsMem function


## -description


The <b>ReallocADsMem</b> function reallocates and copies an existing memory block.


## -parameters




### -param pOldMem [in]

Type: <b>LPVOID</b>

Pointer to the memory to copy. <b>ReallocADsMem</b> will free this memory with <a href="https://msdn.microsoft.com/e43f050a-5b96-406e-87ed-88a39ea747da">FreeADsMem</a> after it has been copied. If additional memory cannot be allocated, this memory is not freed. This memory must have been allocated with the <a href="https://msdn.microsoft.com/df98a728-596b-4541-974a-5690e510ad9f">AllocADsMem</a>, <a href="https://msdn.microsoft.com/1e2b6d42-a879-4a53-a2ce-0e841f6b8543">AllocADsStr</a>, <b>ReallocADsMem</b>, or <a href="https://msdn.microsoft.com/805d45dc-8da4-4c15-a6d1-8967a4da9c24">ReallocADsStr</a> function.

The caller must  free this memory when it is no longer required by passing this pointer to <a href="https://msdn.microsoft.com/e43f050a-5b96-406e-87ed-88a39ea747da">FreeADsMem</a>.


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




<a href="https://msdn.microsoft.com/4f0e90e2-afcc-4cf7-a731-9b38a83ca229">ADSI Functions</a>



<a href="https://msdn.microsoft.com/df98a728-596b-4541-974a-5690e510ad9f">AllocADsMem</a>



<a href="https://msdn.microsoft.com/1e2b6d42-a879-4a53-a2ce-0e841f6b8543">AllocADsStr</a>



<a href="https://msdn.microsoft.com/e43f050a-5b96-406e-87ed-88a39ea747da">FreeADsMem</a>



<a href="https://msdn.microsoft.com/471b8ae7-d3b6-4dd9-aa00-6e1d3ab278a9">ReallocADsMem</a>
 

 

