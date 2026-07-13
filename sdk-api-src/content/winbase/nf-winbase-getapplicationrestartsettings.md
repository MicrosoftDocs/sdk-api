---
UID: NF:winbase.GetApplicationRestartSettings
title: GetApplicationRestartSettings function (winbase.h)
description: Retrieves the restart information registered for the specified process.
helpviewer_keywords: ["GetApplicationRestartSettings","GetApplicationRestartSettings function [Recovery]","recovery.getapplicationrestartsettings","winbase/GetApplicationRestartSettings"]
old-location: recovery\getapplicationrestartsettings.htm
tech.root: Recovery
ms.assetid: bf35437a-9252-4efd-aa3c-be487dafa86e
ms.date: 12/05/2018
ms.keywords: GetApplicationRestartSettings, GetApplicationRestartSettings function [Recovery], recovery.getapplicationrestartsettings, winbase/GetApplicationRestartSettings
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - GetApplicationRestartSettings
 - winbase/GetApplicationRestartSettings
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-windowserrorreporting-l1-1-3.dll
 - api-ms-win-core-windowserrorreporting-l1-1-2.dll
 - api-ms-win-core-windowserrorreporting-l1-1-1.dll
 - Kernel32.dll
 - API-MS-Win-Core-Windowserrorreporting-l1-1-0.dll
 - KernelBase.dll
api_name:
 - GetApplicationRestartSettings
---

# GetApplicationRestartSettings function


## -description

Retrieves  the restart information registered for the specified process.

## -parameters

### -param hProcess [in]

A handle to the process. This handle must have the PROCESS_VM_READ access right.

### -param pwzCommandline [out, optional]

A pointer to a buffer that receives the restart command line specified by the application when it called the <a href="/windows/desktop/api/winbase/nf-winbase-registerapplicationrestart">RegisterApplicationRestart</a> function. The maximum size of the command line, in characters, is RESTART_MAX_CMD_LINE. Can be <b>NULL</b> if <i>pcchSize</i> is zero.

### -param pcchSize [in, out]

On input, specifies the size of the <i>pwzCommandLine</i> buffer, in characters. 

If the buffer is not large enough to receive the command line, the function fails with HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER) and sets this parameter to the required buffer size, in characters.

On output, specifies the size of the buffer that was used.

To determine the required buffer size, set <i>pwzCommandLine</i> to <b>NULL</b> and this parameter to zero. The size includes one for the <b>null</b>-terminator character. Note that the function returns S_OK, not HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER) in this case.

### -param pdwFlags [out, optional]

A pointer to a variable that receives the flags specified by the application when it called the <a href="/windows/desktop/api/winbase/nf-winbase-registerapplicationrestart">RegisterApplicationRestart</a> function.

## -returns

This function returns <b>S_OK</b> on success or one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
The application did not register for restart.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER)</b></dt>
</dl>
</td>
<td width="60%">
The <i>pwzCommandLine</i> buffer is too small. The function returns the required buffer size in <i>pcchSize</i>. Use the required size to reallocate the buffer.

</td>
</tr>
</table>

## -remarks

This information is available only for the current process; you cannot call this function after your program is restarted to get the restart command line. To get the command line after a restart, access the <i>argv</i> parameter of your <b>main</b> function.


#### Examples

The following example shows how to get the restart settings specified when you called the <a href="/windows/desktop/api/winbase/nf-winbase-registerapplicationrestart">RegisterApplicationRestart</a> function.


```cpp
#include <windows.h>
#include <stdio.h>


void wmain(int argc, WCHAR* argv[])
{
    HRESULT hr = S_OK;
    WCHAR wsCommandLine[RESTART_MAX_CMD_LINE + 1];
    DWORD cchCmdLine = sizeof(wsCommandLine) / sizeof(WCHAR);
    DWORD dwFlags = 0;
    LPWSTR pwsCmdLine = NULL;
    UNREFERENCED_PARAMETER(argv);
    UNREFERENCED_PARAMETER(argc);

    wprintf(L"Registering for restart...\n");
    hr = RegisterApplicationRestart(L"/restart -f .\\filename.ext", 0);
    if (FAILED(hr))
    {
        wprintf(L"RegisterApplicationRestart failed, 0x%x\n", hr);
        goto cleanup;
    }

    wprintf(L"Get restart command line using static buffer...\n");
    hr = GetApplicationRestartSettings(GetCurrentProcess(), wsCommandLine, &cchCmdLine, &dwFlags);
    if (FAILED(hr))
    {
        wprintf(L"GetApplicationRestartSettings failed, 0x%x\n", hr);
        goto cleanup;
    }

    wprintf(L"Command line: %s\n", wsCommandLine);

    wprintf(L"\nGet settings using dynamic buffer...\n");

    cchCmdLine = 0;

    // Returns S_OK instead of ERROR_INSUFFICIENT_BUFFER when pBuffer is NULL and size is 0.
    hr = GetApplicationRestartSettings(GetCurrentProcess(), (PWSTR)pwsCmdLine, &cchCmdLine, &dwFlags);
    if (SUCCEEDED(hr))
    {
        pwsCmdLine = (LPWSTR)malloc(cchCmdLine * sizeof(WCHAR));

        if (pwsCmdLine)
        {
            hr = GetApplicationRestartSettings(GetCurrentProcess(), (PWSTR)pwsCmdLine, &cchCmdLine, &dwFlags);
            if (FAILED(hr))
            {
                wprintf(L"GetApplicationRestartSettings failed with 0x%x\n", hr);
                goto cleanup;
            }

            wprintf(L"Command line: %s\n", pwsCmdLine);
        }
        else
        {
            wprintf(L"Allocating the command-line buffer failed.\n");
        }
    }
    else
    {
        if (hr != HRESULT_FROM_WIN32(ERROR_NOT_FOUND)) // Not a restart.
        {
            wprintf(L"GetApplicationRestartSettings failed with 0x%x\n", hr);
            goto cleanup;
        }
    }

cleanup:

    if (pwsCmdLine)
        free(pwsCmdLine);
}

```

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-registerapplicationrestart">RegisterApplicationRestart</a>