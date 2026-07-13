---
UID: NF:appmodel.PackageFamilyNameFromFullName
title: PackageFamilyNameFromFullName function (appmodel.h)
description: Gets the package family name for the specified package full name.
helpviewer_keywords: ["PackageFamilyNameFromFullName","PackageFamilyNameFromFullName function [App packaging and management]","appmodel/PackageFamilyNameFromFullName","appxpkg.packagefamilynamefromfullname"]
old-location: appxpkg\packagefamilynamefromfullname.htm
tech.root: appxpkg
ms.assetid: 98E95CE5-E970-4A19-BAD3-994DAEC4BEA0
ms.date: 12/05/2018
ms.keywords: PackageFamilyNameFromFullName, PackageFamilyNameFromFullName function [App packaging and management], appmodel/PackageFamilyNameFromFullName, appxpkg.packagefamilynamefromfullname
req.header: appmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PackageFamilyNameFromFullName
 - appmodel/PackageFamilyNameFromFullName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-appmodel-runtime-l1-1-7.dll
 - api-ms-win-appmodel-runtime-l1-1-6.dll
 - api-ms-win-appmodel-runtime-l1-1-5.dll
 - api-ms-win-appmodel-runtime-l1-1-4.dll
 - api-ms-win-appmodel-runtime-l1-1-3.dll
 - Kernel32.dll
 - API-MS-Win-AppModel-Runtime-l1-1-0.dll
 - kernel32legacy.dll
 - Ext-MS-Win-kernel32-package-l1-1-0.dll
 - Kernel.AppCore.dll
 - API-MS-Win-AppModel-RunTime-l1-1-1.dll
 - Ext-MS-Win-Kernel32-package-l1-1-2.dll
 - ext-ms-win-kernel32-package-l1-1-1.dll
 - API-MS-Win-AppModel-Runtime-L1-1-2.dll
 - kernelbase.dll
api_name:
 - PackageFamilyNameFromFullName
---

# PackageFamilyNameFromFullName function


## -description

Gets the package family name for the specified package full name.

## -parameters

### -param packageFullName [in]

Type: <b>PCWSTR</b>

The full name of a package.

### -param packageFamilyNameLength [in, out]

Type: <b>UINT32*</b>

On input, the size of the <i>packageFamilyName</i> buffer, in characters. On output, the size of the package family name returned, in characters, including the null terminator.

### -param packageFamilyName [out, optional]

Type: <b>PWSTR</b>

The package family name.

## -returns

Type: <b>LONG</b>

If the function succeeds it returns <b>ERROR_SUCCESS</b>. Otherwise, the function returns an error code. The possible error codes include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The buffer is not large enough to hold the data. The required size is specified  by <i>packageFamilyNameLength</i>.

</td>
</tr>
</table>

## -remarks

For info about string size limits, see <a href="/windows/desktop/appxpkg/identity-constants">Identity constants</a>.


#### Examples


```cpp
#define _UNICODE 1
#define UNICODE 1

#include <Windows.h>
#include <appmodel.h>
#include <malloc.h>
#include <stdio.h>

int ShowUsage();
void FullNameToFamilyName(__in PCWSTR fullName);

int ShowUsage()
{
    wprintf(L"Usage: PackageFamilyNameFromFullName <fullname> [<fullname>...]\n");
    return 1;
}

int __cdecl wmain(__in int argc, __in_ecount(argc) WCHAR * argv[])
{
    if (argc <= 1)
        return ShowUsage();

    for (int i=1; i<argc; ++i)
        FullNameToFamilyName(argv[i]);

    return 0;
}

void FullNameToFamilyName(__in PCWSTR fullName)
{
    wprintf(L"FullName: %s\n", fullName);
    UINT32 length = 0;
    LONG rc = PackageFamilyNameFromFullName(fullName, &length, NULL);
    if (rc == ERROR_SUCCESS)
    {
        wprintf(L"PackageFamilyNameFromFullName unexpectedly succeeded\n");
        return;
    }
    else if (rc != ERROR_INSUFFICIENT_BUFFER)
    {
        wprintf(L"Error %d in PackageFamilyNameFromFullName\n", rc);
        return;
    }

    PWSTR familyName = (PWSTR) malloc(length * sizeof(WCHAR));
    if (familyName == NULL)
    {
        wprintf(L"Error allocating memory\n");
        return;
    }

    rc = PackageFamilyNameFromFullName(fullName, &length, familyName);
    if (rc != ERROR_SUCCESS)
        wprintf(L"Error %d converting PackageFamilyName to FullName\n", rc);
    else
        wprintf(L"Package Family Name = %s\n", familyName);

    free(familyName);
}

```

## -see-also

<a href="/windows/desktop/api/appmodel/nf-appmodel-getcurrentpackagefamilyname">GetCurrentPackageFamilyName</a>



<a href="/windows/desktop/api/appmodel/nf-appmodel-getpackagefamilyname">GetPackageFamilyName</a>



<a href="/windows/desktop/api/appmodel/nf-appmodel-packagefamilynamefromid">PackageFamilyNameFromId</a>



<a href="/windows/desktop/api/appmodel/nf-appmodel-packagefullnamefromid">PackageFullNameFromId</a>



<a href="/windows/desktop/api/appmodel/nf-appmodel-packageidfromfullname">PackageIdFromFullName</a>



<a href="/windows/desktop/api/appmodel/nf-appmodel-packagenameandpublisheridfromfamilyname">PackageNameAndPublisherIdFromFamilyName</a>