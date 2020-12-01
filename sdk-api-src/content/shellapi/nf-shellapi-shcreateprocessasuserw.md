---
UID: NF:shellapi.SHCreateProcessAsUserW
title: SHCreateProcessAsUserW function (shellapi.h)
description: Creates a new user-mode process and its primary thread to run a specified executable file.
helpviewer_keywords: ["SHCreateProcessAsUserW","SHCreateProcessAsUserW function [Windows Shell]","_win32_SHCreateProcessAsUserW","_win32_SHCreateProcessAsUserW_cpp","shell.SHCreateProcessAsUserW","shellapi/SHCreateProcessAsUserW"]
old-location: shell\SHCreateProcessAsUserW.htm
tech.root: shell
ms.assetid: 78548eaf-6907-41e3-9c22-848d0d159085
ms.date: 12/05/2018
ms.keywords: SHCreateProcessAsUserW, SHCreateProcessAsUserW function [Windows Shell], _win32_SHCreateProcessAsUserW, _win32_SHCreateProcessAsUserW_cpp, shell.SHCreateProcessAsUserW, shellapi/SHCreateProcessAsUserW
req.header: shellapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHCreateProcessAsUserW (Unicode)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHCreateProcessAsUserW
 - shellapi/SHCreateProcessAsUserW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHCreateProcessAsUserW
 - SHCreateProcessAsUserW
---

# SHCreateProcessAsUserW function


## -description

<p class="CCE_Message">[<b>SHCreateProcessAsUserW</b> is not implemented under Windows XP or later systems.]

Creates a new user-mode process and its primary thread to run a specified executable file.

## -parameters

### -param pscpi [in, out]

Type: <b>PSHCREATEPROCESSINFOW</b>

A pointer to an <a href="/windows/desktop/api/shellapi/ns-shellapi-shcreateprocessinfow">SHCREATEPROCESSINFOW</a> structure with information on how to create the process.

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if successful, or <b>FALSE</b> if not. To retrieve extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function is similar to <a href="/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information">ShellExecuteEx</a> with <b>runas</b> as the verb. However, <b>SHCreateProcessAsUserW</b> creates a process that runs in the security context of the user represented by the <b>hUserToken</b> member of the structure pointed to by <i>pscpi</i>. The <b>lpProcessInformation</b> member can be used to return a <a href="/windows/desktop/api/processthreadsapi/ns-processthreadsapi-process_information">PROCESS_INFORMATION</a> structure with information on the new process.

The <b>runas</b> verb must be supported by the executable file's <a href="/windows/desktop/shell/fa-file-types">file type</a>. The .exe file type supports <b>runas</b>. Use the <a href="/windows/desktop/api/shlwapi/nf-shlwapi-assocquerystringa">AssocQueryString</a> function to check whether <b>runas</b> is supported by other file types. The following code fragment illustrates the syntax.
			
				


```
AssocQueryString(0, ASSOCSTR_COMMAND, pszFile, TEXT("runas"), NULL, &cchVerb)
```


For a discussion of how to use the Shell to launch applications, see <a href="/windows/desktop/shell/launch">Launching Applications</a>.

<b>SHCreateProcessAsUserW</b> is not supported under Windows XP. Users requiring similar functionality should examine <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>, <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera">CreateProcessAsUser</a>, <a href="/windows/desktop/api/winbase/nf-winbase-createprocesswithlogonw">CreateProcessWithLogonW</a> and <a href="/windows/desktop/api/shellapi/nf-shellapi-shellexecuteexa">ShellExecuteEx</a>, carefully evaluating each based on required functionality and security. <a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations">IQueryAssociations</a> can be used to extract information used with <b>CreateProcess</b>, if necessary.

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera">CreateProcessAsUser</a>



<a href="/windows/desktop/api/winbase/nf-winbase-createprocesswithlogonw">CreateProcessWithLogonW</a>



<a href="/windows/desktop/api/shellapi/nf-shellapi-shellexecuteexa">ShellExecuteEx</a>