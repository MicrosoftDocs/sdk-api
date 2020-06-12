---
UID: NF:appmodel.PackageFamilyNameFromId
title: PackageFamilyNameFromId function (appmodel.h)
description: Gets the package family name for the specified package identifier.
helpviewer_keywords: ["PackageFamilyNameFromId","PackageFamilyNameFromId function [App packaging and management]","appmodel/PackageFamilyNameFromId","appxpkg.packagefamilynamefromid"]
old-location: appxpkg\packagefamilynamefromid.htm
tech.root: appxpkg
ms.assetid: 198DAB6B-21D2-4ACB-87DF-B3F4EFBEE323
ms.date: 12/05/2018
ms.keywords: PackageFamilyNameFromId, PackageFamilyNameFromId function [App packaging and management], appmodel/PackageFamilyNameFromId, appxpkg.packagefamilynamefromid
f1_keywords:
- appmodel/PackageFamilyNameFromId
dev_langs:
- c++
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
- PackageFamilyNameFromId
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PackageFamilyNameFromId function


## -description


Gets the package family name for the specified package identifier.


## -parameters




### -param packageId [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/appmodel/ns-appmodel-package_id">PACKAGE_ID</a>*</b>

The package identifier.


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



For info about string size limits, see <a href="https://docs.microsoft.com/windows/desktop/appxpkg/identity-constants">Identity constants</a>.


#### Examples


```cpp
#define _UNICODE 1
#define UNICODE 1

#include <Windows.h>
#include <appmodel.h>
#include <malloc.h>
#include <stdlib.h>
#include <errno.h>
#include <stdio.h>

int ShowUsage();

int ShowUsage()
{
    wprintf(L"Usage: PackageFamilyNameFromId <name> <publisher>\n");
    return 1;
}

int __cdecl wmain(__in int argc, __in_ecount(argc) WCHAR * argv[])
{
    if (argc <= 5)
        return ShowUsage();

    PACKAGE_ID packageId;
    ZeroMemory(&packageId, sizeof(packageId));
    packageId.name = argv[1];
    packageId.publisher = argv[2];

    UINT32 length = 0;
    LONG rc = PackageFamilyNameFromId(&packageId, &length, NULL);
    if (rc == ERROR_SUCCESS)
    {
        wprintf(L"PackageFamilyNameFromId unexpected succeeded\n");
        return 4;
    }
    else if (rc != ERROR_INSUFFICIENT_BUFFER)
    {
        wprintf(L"Error %d in PackageFamilyNameFromId\n", rc);
        return 5;
    }

    PWSTR familyName = (PWSTR) malloc(length * sizeof(WCHAR));
    if (familyName == NULL)
    {
        wprintf(L"Error allocating memory\n");
        return 6;
    }

    rc = PackageFamilyNameFromId(&packageId, &length, familyName);
    if (rc != ERROR_SUCCESS)
    {
        wprintf(L"Error %d converting Package Id to Family Name\n", rc);
    }
    else
    {
        wprintf(L"Package Family Name = %s\n", familyName);
    }

    free(familyName);

    return rc == ERROR_SUCCESS ? 0 : 7;
}
```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/appmodel/nf-appmodel-getcurrentpackagefamilyname">GetCurrentPackageFamilyName</a>



<a href="https://docs.microsoft.com/windows/desktop/api/appmodel/nf-appmodel-getpackagefamilyname">GetPackageFamilyName</a>



<a href="https://docs.microsoft.com/windows/desktop/api/appmodel/nf-appmodel-packagefamilynamefromfullname">PackageFamilyNameFromFullName</a>



<a href="https://docs.microsoft.com/windows/desktop/api/appmodel/nf-appmodel-packagefullnamefromid">PackageFullNameFromId</a>



<a href="https://docs.microsoft.com/windows/desktop/api/appmodel/nf-appmodel-packageidfromfullname">PackageIdFromFullName</a>



<a href="https://docs.microsoft.com/windows/desktop/api/appmodel/nf-appmodel-packagenameandpublisheridfromfamilyname">PackageNameAndPublisherIdFromFamilyName</a>
 

 

