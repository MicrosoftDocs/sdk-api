---
UID: NF:shellapi.ShellExecuteExA
title: ShellExecuteExA function (shellapi.h)
description: Performs an operation on a specified file. (ShellExecuteExA)
helpviewer_keywords: ["ShellExecuteExA", "shellapi/ShellExecuteExA"]
old-location: shell\ShellExecuteEx.htm
tech.root: shell
ms.assetid: 7850d19c-dadb-44a1-85d9-d5b897edb39f
ms.date: 12/05/2018
ms.keywords: ShellExecuteEx, ShellExecuteEx function [Windows Shell], ShellExecuteExA, ShellExecuteExW, _win32_ShellExecuteEx, _win32_ShellExecuteEx_cpp, shell.ShellExecuteEx, shellapi/ShellExecuteEx, shellapi/ShellExecuteExA, shellapi/ShellExecuteExW
req.header: shellapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ShellExecuteExW (Unicode) and ShellExecuteExA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 3.51 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ShellExecuteExA
 - shellapi/ShellExecuteExA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
 - Ext-MS-Win-shell-shell32-l1-2-0.dll
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
 - windows.storage.dll
api_name:
 - ShellExecuteEx
 - ShellExecuteExA
 - ShellExecuteExW
---

# ShellExecuteExA function


## -description

Performs an operation on a specified file.

## -parameters

### -param pExecInfo [in, out]

Type: <b>SHELLEXECUTEINFO*</b>

A pointer to a <a href="/windows/desktop/api/shellapi/ns-shellapi-shellexecuteinfoa">SHELLEXECUTEINFO</a> structure that contains and receives information about the application being executed.

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if successful; otherwise, <b>FALSE</b>. Call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> for extended error information.

## -remarks

Because <b>ShellExecuteEx</b> can delegate execution to Shell extensions (data sources, context menu handlers, verb implementations) that are activated using Component Object Model (COM), COM should be initialized before <b>ShellExecuteEx</b> is called. Some Shell extensions require the COM single-threaded apartment (STA) type. In that case, COM should be initialized as shown here:

                


``` syntax
CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE)
```

There are instances where <b>ShellExecuteEx</b> does not use one of these types of Shell extension and those instances would not require COM to be initialized at all. Nonetheless, it is good practice to always initialize COM before using this function.

When DLLs are loaded into your process, you acquire a lock known as a <a href="/windows/win32/win7appqual/preventing-hangs-in-windows-applications">loader lock</a>. The <a href="/windows/desktop/Dlls/dllmain">DllMain</a> function always executes under the loader lock. It is important that you do not call <b>ShellExecuteEx</b> while you hold a loader lock. Because <b>ShellExecuteEx</b> is extensible, you could load code that does not function properly in the presence of a loader lock, risking a deadlock and therefore an unresponsive thread.

With multiple monitors, if you specify an <b>HWND</b> and set the <b>lpVerb</b> member of the <a href="/windows/desktop/api/shellapi/ns-shellapi-shellexecuteinfoa">SHELLEXECUTEINFO</a> structure pointed to by <i>lpExecInfo</i> to "Properties", any windows created by <b>ShellExecuteEx</b> might not appear in the correct position.

If the function succeeds, it sets the <b>hInstApp</b> member of the <a href="/windows/desktop/api/shellapi/ns-shellapi-shellexecuteinfoa">SHELLEXECUTEINFO</a> structure to a value greater than 32. If the function fails, <b>hInstApp</b> is set to the <a href="/windows/desktop/api/shellapi/nf-shellapi-shellexecutea">SE_ERR_XXX</a> error value that best indicates the cause of the failure. Although <b>hInstApp</b> is declared as an HINSTANCE for compatibility with 16-bit Windows applications, it is not a true HINSTANCE. It can be cast only to an <b>int</b> and can be compared only to either the value 32 or the SE_ERR_XXX error codes.

The SE_ERR_XXX error values are provided for compatibility with <a href="/windows/desktop/api/shellapi/nf-shellapi-shellexecutea">ShellExecute</a>. To retrieve more accurate error information, use <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. It may return one of the following values.

<table class="clsStd">
<tr>
<th>Error</th>
<th>Description</th>
</tr>
<tr>
<td>ERROR_FILE_NOT_FOUND </td>
<td>The specified file was not found.</td>
</tr>
<tr>
<td>ERROR_PATH_NOT_FOUND </td>
<td>The specified path was not found.</td>
</tr>
<tr>
<td>ERROR_DDE_FAIL </td>
<td>The Dynamic Data Exchange (DDE) transaction failed.</td>
</tr>
<tr>
<td>ERROR_NO_ASSOCIATION </td>
<td>There is no application associated with the specified file name extension.</td>
</tr>
<tr>
<td>ERROR_ACCESS_DENIED </td>
<td>Access to the specified file is denied.</td>
</tr>
<tr>
<td>ERROR_DLL_NOT_FOUND </td>
<td>One of the library files necessary to run the application can't be found.</td>
</tr>
<tr>
<td>ERROR_CANCELLED </td>
<td>The function prompted the user for additional information, but the user canceled the request.</td>
</tr>
<tr>
<td>ERROR_NOT_ENOUGH_MEMORY </td>
<td>There is not enough memory to perform the specified action.</td>
</tr>
<tr>
<td>ERROR_SHARING_VIOLATION </td>
<td>A sharing violation occurred.</td>
</tr>
</table>
 

<b>Opening items from a URL</b> You can register your application to activate when passed URLs. You can also specify which protocols your application supports. See <a href="/windows/desktop/shell/app-registration">Application Registration</a> for more info.

<b>Site chain support</b> As of Windows 8, you can provide a site chain pointer to the <b>ShellExecuteEx</b> function to support item activation with services from that site. See <a href="/windows/desktop/shell/launch">Launching Applications (ShellExecute, ShellExecuteEx, SHELLEXECUTEINFO)</a> for more information. 





> [!NOTE]
> The shellapi.h header defines ShellExecuteEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex">CoInitializeEx</a>



<a href="/windows/desktop/shell/how-to-register-and-implement-a-property-sheet-handler-for-a-control-panel-application">IShellExecuteHook</a>



<a href="/windows/desktop/shell/launch">Launching Applications (ShellExecute, ShellExecuteEx, SHELLEXECUTEINFO)</a>



<a href="/windows/desktop/api/shellapi/nf-shellapi-shellexecutea">ShellExecute</a>
