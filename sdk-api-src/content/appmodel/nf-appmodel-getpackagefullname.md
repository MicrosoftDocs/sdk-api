---
UID: NF:appmodel.GetPackageFullName
title: GetPackageFullName function
author: windows-sdk-content
description: Gets the package full name for the specified process.
old-location: appxpkg\getpackagefullname.htm
old-project: appxpkg
ms.assetid: D1BA8E91-A3D1-454A-A4F6-E3C786F0BD7E
ms.author: windowssdkdev
ms.date: 08/16/2018
ms.keywords: GetPackageFullName, GetPackageFullName function [App packaging and management], appmodel/GetPackageFullName, appxpkg.getpackagefullname
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: appmodel.h
req.include-header: 
req.redist: 
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
 - Ext-MS-Win-kernel32-package-l1-1-0.dll
 - Kernel.AppCore.dll
 - API-MS-Win-AppModel-RunTime-l1-1-1.dll
 - Ext-MS-Win-Kernel32-package-l1-1-2.dll
 - ext-ms-win-kernel32-package-l1-1-1.dll
 - API-MS-Win-AppModel-Runtime-L1-1-2.dll
api_name:
 - GetPackageFullName
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
---

# GetPackageFullName function


## -description


Gets the package full name for the specified process.


## -parameters




### -param hProcess [in]

Type: <b>HANDLE</b>

A handle to the process that has the <b>PROCESS_QUERY_INFORMATION</b> or <b>PROCESS_QUERY_LIMITED_INFORMATION</b> access right. For more information, see <a href="https://msdn.microsoft.com/508a17c4-88cd-431a-a102-00180a7f7ab5">Process Security and Access Rights</a>.


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
The buffer is not large enough to hold the data. The required size is specified  by <i>packageFullNameLength</i>.

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
void ShowProcessPackageFullName(__in const UINT32 pid, __in HANDLE process);

int ShowUsage()
{
    wprintf(L"Usage: GetPackageFullName &lt;pid&gt; [&lt;pid&gt;...]\n");
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
                ShowProcessPackageFullName(pid, process);
                CloseHandle(process);
            }
        }
    }
    return 0;
}

void ShowProcessPackageFullName(__in const UINT32 pid, __in HANDLE process)
{
    wprintf(L"Process %u (handle=%p)\n", pid, process);

    UINT32 length = 0;
    LONG rc = GetPackageFullName(process, &amp;length, NULL);
    if (rc != ERROR_INSUFFICIENT_BUFFER)
    {
        if (rc == APPMODEL_ERROR_NO_PACKAGE)
            wprintf(L"Process has no package identity\n");
        else
            wprintf(L"Error %d in GetPackageFullName\n", rc);
        return;
    }

    PWSTR fullName = (PWSTR) malloc(length * sizeof(*fullName));
    if (fullName == NULL)
    {
        wprintf(L"Error allocating memory\n");
        return;
    }

    rc = GetPackageFullName(process, &amp;length, fullName);
    if (rc != ERROR_SUCCESS)
        wprintf(L"Error %d retrieving PackageFullName\n", rc);
    else
        wprintf(L"%s\n", fullName);

    free(fullName);
}

</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/D5B00C53-1FBF-4245-92D1-FA39713A9EE7">GetCurrentPackageFullName</a>



<a href="https://msdn.microsoft.com/AC239898-9924-4193-9072-7A7EEC2D03E9">GetPackageFamilyName</a>



<a href="https://msdn.microsoft.com/BA5D87F5-72FD-48BE-A104-EC7D1459FD58">GetPackageId</a>



<a href="https://msdn.microsoft.com/0024AF55-295E-49B1-90C2-9144D336529B">PackageFullNameFromId</a>
 

 

