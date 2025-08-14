---
UID: NF:appmodel.PackageNameAndPublisherIdFromFamilyName
title: PackageNameAndPublisherIdFromFamilyName function (appmodel.h)
description: Gets the package name and publisher identifier (ID) for the specified package family name.
helpviewer_keywords: ["PackageNameAndPublisherIdFromFamilyName","PackageNameAndPublisherIdFromFamilyName function [App packaging and management]","appmodel/PackageNameAndPublisherIdFromFamilyName","appxpkg.packagenameandpublisheridfromfamilyname"]
old-location: appxpkg\packagenameandpublisheridfromfamilyname.htm
tech.root: appxpkg
ms.assetid: 4AA5BD75-F865-40D6-9C10-E54C197D47C4
ms.date: 12/05/2018
ms.keywords: PackageNameAndPublisherIdFromFamilyName, PackageNameAndPublisherIdFromFamilyName function [App packaging and management], appmodel/PackageNameAndPublisherIdFromFamilyName, appxpkg.packagenameandpublisheridfromfamilyname
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
 - PackageNameAndPublisherIdFromFamilyName
 - appmodel/PackageNameAndPublisherIdFromFamilyName
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
 - Kernel.AppCore.dll
 - API-MS-Win-AppModel-RunTime-l1-1-1.dll
 - API-MS-Win-AppModel-Runtime-L1-1-2.dll
api_name:
 - PackageNameAndPublisherIdFromFamilyName
---

# PackageNameAndPublisherIdFromFamilyName function


## -description

Gets the package name and publisher identifier (ID) for the specified package family name.

## -parameters

### -param packageFamilyName [in]

Type: <b>PCWSTR</b>

The family name of a package.

### -param packageNameLength [in, out]

Type: <b>UINT32*</b>

On input, the size of the <i>packageName</i> buffer, in characters. On output, the size of the package name returned, in characters, including the null-terminator.

### -param packageName [out, optional]

Type: <b>PWSTR</b>

The package name.

### -param packagePublisherIdLength [in, out]

Type: <b>UINT32*</b>

On input, the size of the <i>packagePublishId</i> buffer, in characters. On output, the size of the publisher ID returned, in characters, including the null-terminator.

### -param packagePublisherId [out, optional]

Type: <b>PWSTR</b>

The package publisher ID.

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
One of the buffers is not large enough to hold the data. The required sizes are specified  by <i>packageNameLength</i> and <i>packagePublisherIdLength</i>.

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
void FamilyNameToNameAndPublisherId(__in PCWSTR familyName);

int ShowUsage()
{
    wprintf(L"Usage: PackageNameAndPublisherIdFromFamilyName <familyname> [<familyname>...]\n");
    return 1;
}

int __cdecl wmain(__in int argc, __in_ecount(argc) WCHAR * argv[])
{
    if (argc <= 1)
        return ShowUsage();

    for (int i=1; i<argc; ++i)
        FamilyNameToNameAndPublisherId(argv[i]);

    return 0;
}

void FamilyNameToNameAndPublisherId(__in PCWSTR familyName)
{
    wprintf(L"FamilyName: %s\n", familyName);
    UINT32 nameLength = 0;
    UINT32 publisherIdLength = 0;
    LONG rc = PackageNameAndPublisherIdFromFamilyName(familyName, &nameLength, NULL, &publisherIdLength, NULL);
    if (rc == ERROR_SUCCESS)
    {
        wprintf(L"PackageNameAndPublisherIdFromFamilyName unexpectedly succeeded\n");
        return;
    }
    else if (rc != ERROR_INSUFFICIENT_BUFFER)
    {
        wprintf(L"Error %d in PackageNameAndPublisherIdFromFamilyName\n", rc);
        return;
    }

    PWSTR name = (PWSTR) malloc(nameLength * sizeof(WCHAR));
    if (name == NULL)
    {
        wprintf(L"Error allocating memory\n");
        return;
    }

    PWSTR publisherId = (PWSTR) malloc(publisherIdLength * sizeof(WCHAR));
    if (publisherId == NULL)
    {
        wprintf(L"Error allocating memory\n");
        free(name);
        return;
    }

    rc = PackageNameAndPublisherIdFromFamilyName(familyName, &nameLength, name, &publisherIdLength, publisherId);
    if (rc != ERROR_SUCCESS)
        wprintf(L"Error %d converting PackageFamilyName to Name and PublisherId\n", rc);
    else
    {
        wprintf(L"        Name = %s\n", name);
        wprintf(L"Publisher Id = %s\n", publisherId);
    }

    free(name);
    free(publisherId);
}

```

## -see-also

<a href="/windows/desktop/api/appmodel/nf-appmodel-packagefamilynamefromfullname">PackageFamilyNameFromFullName</a>



<a href="/windows/desktop/api/appmodel/nf-appmodel-packagefamilynamefromid">PackageFamilyNameFromId</a>



<a href="/windows/desktop/api/appmodel/nf-appmodel-packagefullnamefromid">PackageFullNameFromId</a>



<a href="/windows/desktop/api/appmodel/nf-appmodel-packageidfromfullname">PackageIdFromFullName</a>