---
UID: NF:appmodel.GetApplicationUserModelIdFromToken
title: GetApplicationUserModelIdFromToken function
author: windows-sdk-content
description: Gets the application user model ID for the specified token.
old-location: appxpkg\getapplicationusermodelidfromtoken.htm
old-project: appxpkg
ms.assetid: 80036518-927E-4CD0-B499-8EA472AB7E5A
ms.author: windowssdkdev
ms.date: 06/22/2018
ms.keywords: GetApplicationUserModelIdFromToken, GetApplicationUserModelIdFromToken function [App packaging and management], appmodel/GetApplicationUserModelIdFromToken, appxpkg.getapplicationusermodelidfromtoken
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: PackageOrigin
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-AppModel-Runtime-l1-1-0.dll
 - kernel32legacy.dll
 - Kernel.AppCore.dll
 - API-MS-Win-AppModel-RunTime-l1-1-1.dll
 - API-MS-Win-AppModel-Runtime-L1-1-2.dll
api_name:
 - GetApplicationUserModelIdFromToken
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
---

# GetApplicationUserModelIdFromToken function


## -description


Gets the <a href="https://msdn.microsoft.com/15E35DCF-C6C1-446A-B09B-6428F9C8A677">application user model ID</a> for the specified token.


## -parameters




### -param token [in]

A token that contains the application identity. This handle must have the <b>PROCESS_QUERY_LIMITED_INFORMATION</b> access right. For more info, see <a href="https://msdn.microsoft.com/508a17c4-88cd-431a-a102-00180a7f7ab5">Process Security and Access Rights</a>.


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



For info about string size limits, see <a href="https://msdn.microsoft.com/C4F81822-B502-4360-AEA4-829F1AB926BF">Identity constants</a>.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>/***************************************************
*                                                  *
*   Copyright (C) Microsoft. All rights reserved.  *
*                                                  *
***************************************************/

#define _UNICODE 1
#define UNICODE 1

#include &lt;Windows.h&gt;
#include &lt;appmodel.h&gt;
#include &lt;appmodelp.h&gt;
#include &lt;malloc.h&gt;
#include &lt;stdlib.h&gt;
#include &lt;stdio.h&gt;

int ShowUsage();
void ShowProcessApplicationUserModelId(__in const UINT32 pid, __in HANDLE token);

int ShowUsage()
{
    wprintf(L"Usage: GetApplicationUserModelIdFromToken &lt;pid&gt; [&lt;pid&gt;...]\n");
    return 1;
}

int __cdecl wmain(__in int argc, __in_ecount(argc) WCHAR * argv[])
{
    if (argc &lt;= 1)
        return ShowUsage();

    for (int i=1; i&lt;argc; ++i)
    {
        UINT32 pid = wcstoul(argv[i], NULL, 10);
        if (pid &gt; 0)
        {
            HANDLE process = OpenProcess(PROCESS_QUERY_LIMITED_INFORMATION, FALSE, pid);
            if (process == NULL)
                wprintf(L"Error %d in OpenProcess (pid=%u)\n", GetLastError(), pid);
            else
            {
                HANDLE token;
                if (!OpenProcessToken(process, TOKEN_QUERY, &amp;token))
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
    LONG rc = GetApplicationUserModelIdFromToken(token, &amp;length, NULL);
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

    rc = GetApplicationUserModelIdFromToken(token, &amp;length, applicationUserModelId);
    if (rc != ERROR_SUCCESS)
        wprintf(L"Error %d retrieving ApplicationUserModelId\n", rc);
    else
        wprintf(L"%s\n", applicationUserModelId);

    free(applicationUserModelId);
}
</pre>
</td>
</tr>
</table></span></div>


