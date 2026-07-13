---
UID: NF:appmodel.GetApplicationUserModelIdFromToken
title: GetApplicationUserModelIdFromToken function (appmodel.h)
description: Gets the application user model ID for the specified token.
helpviewer_keywords: ["GetApplicationUserModelIdFromToken","GetApplicationUserModelIdFromToken function [App packaging and management]","appmodel/GetApplicationUserModelIdFromToken","appxpkg.getapplicationusermodelidfromtoken"]
old-location: appxpkg\getapplicationusermodelidfromtoken.htm
tech.root: appxpkg
ms.assetid: 80036518-927E-4CD0-B499-8EA472AB7E5A
ms.date: 12/05/2018
ms.keywords: GetApplicationUserModelIdFromToken, GetApplicationUserModelIdFromToken function [App packaging and management], appmodel/GetApplicationUserModelIdFromToken, appxpkg.getapplicationusermodelidfromtoken
req.header: appmodel.h
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetApplicationUserModelIdFromToken
 - appmodel/GetApplicationUserModelIdFromToken
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
 - GetApplicationUserModelIdFromToken
---

# GetApplicationUserModelIdFromToken function


## -description

Gets the <a href="/windows/desktop/appxpkg/appx-packaging-glossary">application user model ID</a> for the specified token.

## -parameters

### -param token [in]

A token that contains the application identity. This handle must have the <b>PROCESS_QUERY_LIMITED_INFORMATION</b> access right. For more info, see <a href="/windows/desktop/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>.

### -param applicationUserModelIdLength [in, out]

On input, the size of the  <i>applicationUserModelId</i> buffer, in wide characters. On success, the size of the buffer used, including the null terminator.

### -param applicationUserModelId [out]

A pointer to a buffer that receives the application user model ID.

## -returns

If the function succeeds it returns <b>ERROR_SUCCESS</b>. Otherwise, the function returns an error code. The possible error codes include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>APPMODEL_ERROR_NO_APPLICATION</b></dt>
</dl>
</td>
<td width="60%">
The token has no application identity.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The buffer is not large enough to hold the data. The required size is specified  by <i>applicationUserModelIdLength</i>.

</td>
</tr>
</table>

## -remarks

For info about string size limits, see <a href="/windows/desktop/appxpkg/identity-constants">Identity constants</a>.


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
void ShowProcessApplicationUserModelId(__in const UINT32 pid, __in HANDLE token);

int ShowUsage()
{
    wprintf(L"Usage: GetApplicationUserModelIdFromToken <pid> [<pid>...]\n");
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
                    ShowProcessApplicationUserModelId(pid, token);
                    CloseHandle(token);
                }
                CloseHandle(process);
            }
        }
    }
    return 0;
}

void ShowProcessApplicationUserModelId(__in const UINT32 pid, __in HANDLE token)
{
    wprintf(L"Process %u (token=%p)\n", pid, token);

    UINT32 length = 0;
    LONG rc = GetApplicationUserModelIdFromToken(token, &length, NULL);
    if (rc != ERROR_INSUFFICIENT_BUFFER)
    {
        if (rc == APPMODEL_ERROR_NO_PACKAGE)
            wprintf(L"Token has no package identity\n");
        else
            wprintf(L"Error %d in GetApplicationUserModelIdFromToken\n", rc);
        return;
    }

    PWSTR applicationUserModelId = (PWSTR) malloc(length * sizeof(*applicationUserModelId));
    if (applicationUserModelId == NULL)
    {
        wprintf(L"Error allocating memory\n");
        return;
    }

    rc = GetApplicationUserModelIdFromToken(token, &length, applicationUserModelId);
    if (rc != ERROR_SUCCESS)
        wprintf(L"Error %d retrieving ApplicationUserModelId\n", rc);
    else
        wprintf(L"%s\n", applicationUserModelId);

    free(applicationUserModelId);
}

```