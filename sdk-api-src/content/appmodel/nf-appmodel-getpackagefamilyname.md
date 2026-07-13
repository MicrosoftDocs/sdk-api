---
UID: NF:appmodel.GetPackageFamilyName
title: GetPackageFamilyName function (appmodel.h)
description: Gets the package family name for the specified process.
helpviewer_keywords: ["GetPackageFamilyName","GetPackageFamilyName function [App packaging and management]","appmodel/GetPackageFamilyName","appxpkg.getpackagefamilyname"]
old-location: appxpkg\getpackagefamilyname.htm
tech.root: appxpkg
ms.assetid: AC239898-9924-4193-9072-7A7EEC2D03E9
ms.date: 12/05/2018
ms.keywords: GetPackageFamilyName, GetPackageFamilyName function [App packaging and management], appmodel/GetPackageFamilyName, appxpkg.getpackagefamilyname
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
 - GetPackageFamilyName
 - appmodel/GetPackageFamilyName
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
 - GetPackageFamilyName
---

# GetPackageFamilyName function


## -description

Gets the package family name for the specified process.

## -parameters

### -param hProcess [in]

Type: <b>HANDLE</b>

A handle to the process that has the <b>PROCESS_QUERY_INFORMATION</b> or <b>PROCESS_QUERY_LIMITED_INFORMATION</b> access right. For more information, see <a href="/windows/desktop/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>.

### -param packageFamilyNameLength [in, out]

Type: <b>UINT32*</b>

On input, the size of the <i>packageFamilyName</i> buffer, in characters. On output, the size of the package family name returned, in characters, including the null-terminator.

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
<dt><b>APPMODEL_ERROR_NO_PACKAGE</b></dt>
</dl>
</td>
<td width="60%">
The process has no package identity.

</td>
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
#include <stdlib.h>
#include <stdio.h>

int ShowUsage();
void ShowProcessPackageFamilyName(__in const UINT32 pid, __in HANDLE process);

int ShowUsage()
{
    wprintf(L"Usage: GetPackageFamilyName <pid> [<pid>...]\n");
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
                ShowProcessPackageFamilyName(pid, process);
                CloseHandle(process);
            }
        }
    }
    return 0;
}

void ShowProcessPackageFamilyName(__in const UINT32 pid, __in HANDLE process)
{
    wprintf(L"Process %u (handle=%p)\n", pid, process);

    UINT32 length = 0;
    LONG rc = GetPackageFamilyName(process, &length, NULL);
    if (rc != ERROR_INSUFFICIENT_BUFFER)
    {
        if (rc == APPMODEL_ERROR_NO_PACKAGE)
            wprintf(L"Process has no package identity\n");
        else
            wprintf(L"Error %d in GetPackageFamilyName\n", rc);
        return;
    }

    PWSTR familyName = (PWSTR) malloc(length * sizeof(*familyName));
    if (familyName == NULL)
    {
        wprintf(L"Error allocating memory\n");
        return;
    }

    rc = GetPackageFamilyName(process, &length, familyName);
    if (rc != ERROR_SUCCESS)
        wprintf(L"Error %d retrieving PackageFamilyName\n", rc);
    else
        wprintf(L"%s\n", familyName);

    free(familyName);
}


```

## -see-also

<a href="/windows/desktop/api/appmodel/nf-appmodel-getcurrentpackagefamilyname">GetCurrentPackageFamilyName</a>



<a href="/windows/desktop/api/appmodel/nf-appmodel-getpackagefullname">GetPackageFullName</a>



<a href="/windows/desktop/api/appmodel/nf-appmodel-getpackageid">GetPackageId</a>



<a href="/windows/desktop/api/appmodel/nf-appmodel-packagefamilynamefromfullname">PackageFamilyNameFromFullName</a>



<a href="/windows/desktop/api/appmodel/nf-appmodel-packagefamilynamefromid">PackageFamilyNameFromId</a>