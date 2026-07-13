---
UID: NF:appmodel.GetPackageFullNameFromToken
title: GetPackageFullNameFromToken function (appmodel.h)
description: Gets the package full name for the specified token.
helpviewer_keywords: ["GetPackageFullNameFromToken","GetPackageFullNameFromToken function [App packaging and management]","appmodel/GetPackageFullNameFromToken","appxpkg.getpackagefullnamefromtoken"]
old-location: appxpkg\getpackagefullnamefromtoken.htm
tech.root: appxpkg
ms.assetid: 7B0D574E-A2F5-4D08-AEFB-9E040BBC729F
ms.date: 12/05/2018
ms.keywords: GetPackageFullNameFromToken, GetPackageFullNameFromToken function [App packaging and management], appmodel/GetPackageFullNameFromToken, appxpkg.getpackagefullnamefromtoken
req.header: appmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - GetPackageFullNameFromToken
 - appmodel/GetPackageFullNameFromToken
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
 - API-MS-Win-AppModel-Runtime-Internal-L1-1-1.dll
 - API-MS-Win-AppModel-Runtime-Internal-L1-1-2.dll
 - API-MS-Win-AppModel-Runtime-Internal-L1-1-3.dll
 - API-MS-Win-AppModel-Runtime-L1-1-0.dll
 - API-MS-Win-AppModel-Runtime-L1-1-1.dll
 - API-MS-Win-AppModel-Runtime-L1-1-2.dll
 - Ext-MS-Win-Kernel32-Package-L1-1-0.dll
 - Ext-MS-Win-Kernel32-Package-L1-1-1.dll
 - Ext-MS-Win-Kernel32-Package-L1-1-2.dll
 - Kernel.AppCore.dll
 - Kernel32Legacy.dll
 - kernelbase.dll
api_name:
 - GetPackageFullNameFromToken
---

# GetPackageFullNameFromToken function


## -description

Gets the package full name for the specified token.

## -parameters

### -param token [in]

A token that contains the package identity.

### -param packageFullNameLength [in, out]

On input, the size of the <i>packageFullName</i> buffer, in characters. On output, the 
      size of the package full name returned, in characters, including the null terminator.

### -param packageFullName [out, optional]

The package full name.

## -returns

If the function succeeds it returns <b>ERROR_SUCCESS</b>. Otherwise, the function 
      returns an error code. The possible error codes include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>APPMODEL_ERROR_NO_PACKAGE</b></dt>
</dl>
</td>
<td width="60%">
The token has no package identity.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The buffer is not large enough to hold the data. The required size is specified  by 
         <i>packageFullNameLength</i>.

</td>
</tr>
</table>

## -remarks

For info about string size limits, see 
     <a href="/windows/desktop/appxpkg/identity-constants">Identity constants</a>.


#### Examples


```cpp
/***************************************************
*                                                  *
*   Copyright (C) Microsoft. All rights reserved.  *
*                                                  *
***************************************************/

#define _UNICODE 1
#define UNICODE 1

#include <Windows.h>
#include <appmodel.h>
#include <appmodelp.h>
#include <malloc.h>
#include <stdlib.h>
#include <stdio.h>

int ShowUsage();
void ShowProcessPackageFullName(__in const UINT32 pid, __in HANDLE token);

int ShowUsage()
{
    wprintf(L"Usage: GetPackageFullNameFromToken <pid> [<pid>...]\n");
    return 1;
}

int __cdecl wmain(__in int argc, __in_ecount(argc) WCHAR * argv[])
{
    if (argc <= 1)
        return ShowUsage();

    for (int i=1; i<argc; ++i)
    {
        UINT32 pid = wcstoul(argv[i], NULL, 10);
        if (pid > 0)
        {
            HANDLE process = OpenProcess(PROCESS_QUERY_LIMITED_INFORMATION, FALSE, pid);
            if (process == NULL)
                wprintf(L"Error %d in OpenProcess (pid=%u)\n", GetLastError(), pid);
            else
            {
                HANDLE token;
                if (!OpenProcessToken(process, TOKEN_QUERY, &token))
                    wprintf(L"Error %d in OpenProcessToken (pid=%u)\n", GetLastError(), pid);
                else
                {
                    ShowProcessPackageFullName(pid, token);
                    CloseHandle(token);
                }
                CloseHandle(process);
            }
        }
    }
    return 0;
}

void ShowProcessPackageFullName(__in const UINT32 pid, __in HANDLE token)
{
    wprintf(L"Process %u (token=%p)\n", pid, token);

    UINT32 length = 0;
    LONG rc = GetPackageFullNameFromToken(token, &length, NULL);
    if (rc != ERROR_INSUFFICIENT_BUFFER)
    {
        if (rc == APPMODEL_ERROR_NO_PACKAGE)
            wprintf(L"Token has no package identity\n");
        else
            wprintf(L"Error %d in GetPackageFullNameFromToken\n", rc);
        return;
    }

    PWSTR fullName = (PWSTR) malloc(length * sizeof(*fullName));
    if (fullName == NULL)
    {
        wprintf(L"Error allocating memory\n");
        return;
    }

    rc = GetPackageFullNameFromToken(token, &length, fullName);
    if (rc != ERROR_SUCCESS)
        wprintf(L"Error %d retrieving PackageFullName\n", rc);
    else
        wprintf(L"%s\n", fullName);

    free(fullName);
}
```