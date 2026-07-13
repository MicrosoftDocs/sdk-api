---
UID: NF:appmodel.PackageIdFromFullName
title: PackageIdFromFullName function (appmodel.h)
description: Gets the package identifier (ID) for the specified package full name.
helpviewer_keywords: ["PackageIdFromFullName","PackageIdFromFullName function [App packaging and management]","appmodel/PackageIdFromFullName","appxpkg.packageidfromfullname"]
old-location: appxpkg\packageidfromfullname.htm
tech.root: appxpkg
ms.assetid: EED832F8-E4F7-4A0F-93E2-451F78F67767
ms.date: 12/05/2018
ms.keywords: PackageIdFromFullName, PackageIdFromFullName function [App packaging and management], appmodel/PackageIdFromFullName, appxpkg.packageidfromfullname
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
 - PackageIdFromFullName
 - appmodel/PackageIdFromFullName
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
api_name:
 - PackageIdFromFullName
---

# PackageIdFromFullName function


## -description

Gets the package identifier (ID) for the specified package full name.

## -parameters

### -param packageFullName [in]

Type: <b>PCWSTR</b>

The full name of a package.

### -param flags [in]

Type: <b>const UINT32</b>

The <a href="/windows/desktop/appxpkg/package-constants">package constants</a> that specify how package information is retrieved. The <b>PACKAGE_INFORMATION_*</b> flags are supported.

### -param bufferLength [in, out]

Type: <b>UINT32*</b>

On input, the size of <i>buffer</i>, in bytes. On output, the size of the data returned, in bytes.

### -param buffer [out, optional]

Type: <b>BYTE*</b>

The package ID, represented as a <a href="/windows/desktop/api/appmodel/ns-appmodel-package_id">PACKAGE_ID</a> structure.

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
The buffer is not large enough to hold the data. The required size is specified  by <i>bufferLength</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The package is not installed for the user.

</td>
</tr>
</table>

## -remarks

If <i>flags</i> specifies <b>PACKAGE_INFORMATION_BASIC</b>, the following fields are retrieved:

<ul>
<li><b>name</b></li>
<li><b>processorArchitecture</b></li>
<li><b>publisherId</b></li>
<li><b>resourceId</b></li>
<li><b>version</b></li>
</ul>
If <i>flags</i> specifies <b>PACKAGE_INFORMATION_FULL</b>, the following fields are retrieved:

<ul>
<li><b>name</b></li>
<li><b>processorArchitecture</b></li>
<li><b>publisher</b></li>
<li><b>publisherId</b></li>
<li><b>resourceId</b></li>
<li><b>version</b></li>
</ul>
A request for <b>PACKAGE_INFORMATION_FULL</b> succeeds only if the package corresponding to <i>packageFullName</i> is installed for and accessible to the current user. If the package full name is syntactically correct but does not correspond to a package that is installed for and accessible to the current user, the function returns <b>ERROR_NOT_FOUND</b>.

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
void FullNameToId(__in PCWSTR fullName, __in const UINT32 flags);
void ShowPackageId(__in const PACKAGE_ID * packageId);

int ShowUsage()
{
    wprintf(L"Usage: PackageIdFromFullName <[flags]fullname> [<[flags]fullname>...]\n"
            L"flags:\n"
            L"    ? = Basic information (PACKAGE_INFORMATION_BASIC)\n"
            L"    * = Full information (PACKAGE_INFORMATION_FULL)\n"
            L"Default = Basic\n");
    return 1;
}

int __cdecl wmain(__in int argc, __in_ecount(argc) WCHAR * argv[])
{
    if (argc <= 1)
        return ShowUsage();

    for (int i=1; i<argc; ++i)
    {
        PCWSTR fullName = argv[i];
        UINT32 flags = PACKAGE_INFORMATION_BASIC;
        if (*fullName != L'\0')
        {
            if (*fullName == L'?')
            {
                flags = PACKAGE_INFORMATION_BASIC;
                ++fullName;
            }
            else if (*fullName == L'*')
            {
                flags = PACKAGE_INFORMATION_FULL;
                ++fullName;
            }
        }
        FullNameToId(fullName, flags);
    }

    return 0;
}

void FullNameToId(__in PCWSTR fullName, __in const UINT32 flags)
{
    wprintf(L"FullName: %s%s\n", fullName, ((flags & PACKAGE_INFORMATION_FULL) == 0 ? L"  [BASIC]" : L"  [FULL]"));
    UINT32 length = 0;
    LONG rc = PackageIdFromFullName(fullName, flags, &length, NULL);
    if (rc == ERROR_SUCCESS)
    {
        wprintf(L"PackageIdFromFullName unexpected succeeded\n");
        return;
    }
    else if (rc != ERROR_INSUFFICIENT_BUFFER)
    {
        wprintf(L"Error %d in PackageIdFromFullName\n", rc);
        return;
    }

    BYTE * buffer = (PBYTE) malloc(length);
    if (buffer == NULL)
    {
        wprintf(L"Error allocating memory\n");
        return;
    }

    rc = PackageIdFromFullName(fullName, flags, &length, buffer);
    if (rc != ERROR_SUCCESS)
        wprintf(L"Error %d converting Package Full Name to Id\n", rc);
    else
    {
        ShowPackageId((PACKAGE_ID *) buffer);
    }

    free(buffer);
}

void ShowPackageId(__in const PACKAGE_ID * packageId)
{
    wprintf(L"    Name        : %s\n", packageId->name);
    if (packageId->publisher != NULL)
        wprintf(L"    Publisher   : %s\n", packageId->publisher);
    if (packageId->publisherId != NULL)
        wprintf(L"    PublisherId : %s\n", packageId->publisherId);
    wprintf(L"    Version     : %hu.%hu.%hu.%hu\n",
            packageId->version.Major,
            packageId->version.Minor,
            packageId->version.Build,
            packageId->version.Revision);
    wprintf(L"    Architecture: %u\n", packageId->processorArchitecture);
    if (packageId->resourceId != NULL)
        wprintf(L"    Resource    : %s\n", packageId->resourceId);
}

```

## -see-also

<a href="/windows/desktop/api/appmodel/nf-appmodel-getcurrentpackageid">GetCurrentPackageId</a>



<a href="/windows/desktop/api/appmodel/nf-appmodel-getpackageid">GetPackageId</a>



<a href="/windows/desktop/api/appmodel/nf-appmodel-packagefamilynamefromfullname">PackageFamilyNameFromFullName</a>



<a href="/windows/desktop/api/appmodel/nf-appmodel-packagefamilynamefromid">PackageFamilyNameFromId</a>



<a href="/windows/desktop/api/appmodel/nf-appmodel-packagefullnamefromid">PackageFullNameFromId</a>



<a href="/windows/desktop/api/appmodel/nf-appmodel-packagenameandpublisheridfromfamilyname">PackageNameAndPublisherIdFromFamilyName</a>