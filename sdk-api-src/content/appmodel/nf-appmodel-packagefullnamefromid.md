---
UID: NF:appmodel.PackageFullNameFromId
title: PackageFullNameFromId function
author: windows-sdk-content
description: Gets the package full name for the specified package identifier (ID).
old-location: appxpkg\packagefullnamefromid.htm
tech.root: appxpkg
ms.assetid: 0024AF55-295E-49B1-90C2-9144D336529B
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: PackageFullNameFromId, PackageFullNameFromId function [App packaging and management], appmodel/PackageFullNameFromId, appxpkg.packagefullnamefromid
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
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
 - PackageFullNameFromId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PackageFullNameFromId function


## -description


Gets the package full name for the specified package identifier (ID).


## -parameters




### -param packageId [in]

Type: <b>const <a href="https://msdn.microsoft.com/4B15281A-2227-47B7-A750-0A01DB8543FC">PACKAGE_ID</a>*</b>

The package ID.


### -param packageFullNameLength [in, out]

Type: <b>UINT32*</b>

On input, the size of the <i>packageFullName</i> buffer, in characters. On output, the size of the package full name returned, in characters, including the null terminator.


### -param packageFullName [out, optional]

Type: <b>PWSTR</b>

The package full name.


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
The buffer is not large enough to hold the data. The required size is specified  by <i>packageFullNameLength</i>.

</td>
</tr>
</table>
 




## -remarks



For info about string size limits, see <a href="https://msdn.microsoft.com/C4F81822-B502-4360-AEA4-829F1AB926BF">Identity constants</a>.


#### Examples


```
#define _UNICODE 1
#define UNICODE 1

#include <Windows.h>
#include <appmodel.h>
#include <malloc.h>
#include <stdlib.h>
#include <errno.h>
#include <stdio.h>

int ShowUsage();
bool ParseArchitecture(__in PCWSTR architectureString, __out UINT32 * architecture);
bool ParseVersion(__in PCWSTR versionString, __out PACKAGE_VERSION * version);

int ShowUsage()
{
    wprintf(L"Usage: PackageFullNameFromId <name><version> <arch> <resourceid> <publisher>\n");
    return 1;
}

int __cdecl wmain(__in int argc, __in_ecount(argc) WCHAR * argv[])
{
    if (argc <= 5)
        return ShowUsage();

    PACKAGE_ID packageId;
    ZeroMemory(&packageId, sizeof(packageId));
    packageId.name = argv[1];
    if (!ParseVersion(argv[2], &packageId.version))
        return 2;
    if (!ParseArchitecture(argv[3], &packageId.processorArchitecture))
        return 3;
    packageId.resourceId = argv[4];
    packageId.publisher = argv[5];

    UINT32 length = 0;
    LONG rc = PackageFullNameFromId(&packageId, &length, NULL);
    if (rc == ERROR_SUCCESS)
    {
        wprintf(L"PackageFullNameFromId unexpectedly succeeded\n");
        return 4;
    }
    else if (rc != ERROR_INSUFFICIENT_BUFFER)
    {
        wprintf(L"Error %d in PackageFullNameFromId\n", rc);
        return 5;
    }

    PWSTR fullName = (PWSTR) malloc(length * sizeof(WCHAR));
    if (fullName == NULL)
    {
        wprintf(L"Error allocating memory\n");
        return 6;
    }

    rc = PackageFullNameFromId(&packageId, &length, fullName);
    if (rc != ERROR_SUCCESS)
        wprintf(L"Error %d converting Package Id to Full Name\n", rc);
    else
        wprintf(L"Package Full Name = %s\n", fullName);

    free(fullName);

    return rc == ERROR_SUCCESS ? 0 : 7;
}

bool ParseArchitecture(__in PCWSTR architectureString, __out UINT32 * architecture)
{
    if (_wcsicmp(architectureString, L"neutral") == 0)
        *architecture = PROCESSOR_ARCHITECTURE_NEUTRAL;
    else if (_wcsicmp(architectureString, L"x86") == 0)
        *architecture = PROCESSOR_ARCHITECTURE_INTEL;
    else if (_wcsicmp(architectureString, L"x64") == 0)
        *architecture = PROCESSOR_ARCHITECTURE_AMD64;
    else if (_wcsicmp(architectureString, L"arm") == 0)
        *architecture = PROCESSOR_ARCHITECTURE_ARM;
    else
    {
        wprintf(L"Invalid architecture\n");
        return false;
    }
    return true;
}

bool ParseVersion(__in PCWSTR versionString, __out PACKAGE_VERSION * version)
{
    PWSTR s = (PWSTR) versionString;

    ULONG n = wcstoul(s, &s, 10);
    if (((n == 0) || (n > 65535)) && (errno == ERANGE)) {
        wprintf(L"Invalid Version (Major)\n");
        return false;
    }
    version->Major = (USHORT) n;

    if (*s != L'.')
    {
        wprintf(L"Invalid Version\n");
        return false;
    }

    n = wcstoul(++s, &s, 10);
    if (((n == 0) || (n > 65535)) && (errno == ERANGE)) {
        wprintf(L"Invalid Version (Minor)\n");
        return false;
    }
    version->Minor = (USHORT) n;

    if (*s != L'.')
    {
        wprintf(L"Invalid Version\n");
        return false;
    }

    n = wcstoul(++s, &s, 10);
    if (((n == 0) || (n > 65535)) && (errno == ERANGE)) {
        wprintf(L"Invalid Version (Build)\n");
        return false;
    }
    version->Build = (USHORT) n;

    if (*s != L'.')
    {
        wprintf(L"Invalid Version\n");
        return false;
    }

    n = wcstoul(++s, &s, 10);
    if (((n == 0) || (n > 65535)) && (errno == ERANGE)) {
        wprintf(L"Invalid Version (Revision)\n");
        return false;
    }
    version->Revision = (USHORT) n;

    return true;
}

```





## -see-also




<a href="https://msdn.microsoft.com/D5B00C53-1FBF-4245-92D1-FA39713A9EE7">GetCurrentPackageFullName</a>



<a href="https://msdn.microsoft.com/D1BA8E91-A3D1-454A-A4F6-E3C786F0BD7E">GetPackageFullName</a>



<a href="https://msdn.microsoft.com/98E95CE5-E970-4A19-BAD3-994DAEC4BEA0">PackageFamilyNameFromFullName</a>



<a href="https://msdn.microsoft.com/198DAB6B-21D2-4ACB-87DF-B3F4EFBEE323">PackageFamilyNameFromId</a>



<a href="https://msdn.microsoft.com/EED832F8-E4F7-4A0F-93E2-451F78F67767">PackageIdFromFullName</a>



<a href="https://msdn.microsoft.com/4AA5BD75-F865-40D6-9C10-E54C197D47C4">PackageNameAndPublisherIdFromFamilyName</a>
 

 

