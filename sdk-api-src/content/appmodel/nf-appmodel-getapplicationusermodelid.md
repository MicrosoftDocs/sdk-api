---
UID: NF:appmodel.GetApplicationUserModelId
title: GetApplicationUserModelId function
author: windows-sdk-content
description: Gets the application user model ID for the specified process.
old-location: appxpkg\getapplicationusermodelid.htm
old-project: appxpkg
ms.assetid: FE4E0818-F548-494B-B3BD-FB51DC748451
ms.author: windowssdkdev
ms.date: 04/26/2018
ms.keywords: GetApplicationUserModelId, GetApplicationUserModelId function [App packaging and management], appmodel/GetApplicationUserModelId, appxpkg.getapplicationusermodelid
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
 - GetApplicationUserModelId
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
---

# GetApplicationUserModelId function


## -description


Gets the <a href="https://msdn.microsoft.com/15E35DCF-C6C1-446A-B09B-6428F9C8A677">application user model ID</a> for the specified process.


## -parameters




### -param hProcess [in]

A handle to the process. This handle must have the <b>PROCESS_QUERY_LIMITED_INFORMATION</b> access right. For more info, see <a href="https://msdn.microsoft.com/508a17c4-88cd-431a-a102-00180a7f7ab5">Process Security and Access Rights</a>.


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
The process has no application identity.

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
<pre>#define _UNICODE 1
#define UNICODE 1

#include &lt;Windows.h&gt;
#include &lt;appmodel.h&gt;
#include &lt;malloc.h&gt;
#include &lt;stdlib.h&gt;
#include &lt;stdio.h&gt;

int ShowUsage();
void ShowProcessApplicationUserModelId(__in const UINT32 pid, __in HANDLE process);

int ShowUsage()
{
    wprintf(L"Usage: GetApplicationUserModelId &lt;pid&gt; [&lt;pid&gt;...]\n");
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
                ShowProcessApplicationUserModelId(pid, process);
                CloseHandle(process);
            }
        }
    }
    return 0;
}

void ShowProcessApplicationUserModelId(__in const UINT32 pid, __in HANDLE process)
{
    wprintf(L"Process %u (handle=%p)\n", pid, process);

    UINT32 length = 0;
    LONG rc = GetApplicationUserModelId(process, &amp;length, NULL);
    if (rc != ERROR_INSUFFICIENT_BUFFER)
    {
        if (rc == APPMODEL_ERROR_NO_APPLICATION)
            wprintf(L"Desktop application\n");
        else
            wprintf(L"Error %d in GetApplicationUserModelId\n", rc);
        return;
    }

    PWSTR fullName = (PWSTR) malloc(length * sizeof(*fullName));
    if (fullName == NULL)
    {
        wprintf(L"Error allocating memory\n");
        return;
    }

    rc = GetApplicationUserModelId(process, &amp;length, fullName);
    if (rc != ERROR_SUCCESS)
        wprintf(L"Error %d retrieving ApplicationUserModelId\n", rc);
    else
        wprintf(L"%s\n", fullName);

    free(fullName);
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/562BB225-0922-4FE7-92C0-573A2CCE3195">GetCurrentApplicationUserModelId</a>



<a href="https://msdn.microsoft.com/AC239898-9924-4193-9072-7A7EEC2D03E9">GetPackageFamilyName</a>



<a href="https://msdn.microsoft.com/BA5D87F5-72FD-48BE-A104-EC7D1459FD58">GetPackageId</a>



<a href="https://msdn.microsoft.com/28F45B3B-A61F-44D3-B606-6966AD5866FA">GetPackageInfo</a>



<a href="https://msdn.microsoft.com/BDA0DD87-A36D-486B-BF89-EA5CC105C742">GetPackagePath</a>
 

 

