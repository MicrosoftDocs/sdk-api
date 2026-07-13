---
UID: NF:shellapi.SHEvaluateSystemCommandTemplate
title: SHEvaluateSystemCommandTemplate function (shellapi.h)
description: Enforces strict validation of parameters used in a call to CreateProcess or ShellExecute.
helpviewer_keywords: ["SHEvaluateSystemCommandTemplate","SHEvaluateSystemCommandTemplate function [Windows Shell]","_shell_SHEvaluateSystemCommandTemplate","shell.SHEvaluateSystemCommandTemplate","shellapi/SHEvaluateSystemCommandTemplate"]
old-location: shell\SHEvaluateSystemCommandTemplate.htm
tech.root: shell
ms.assetid: 554b941d-7d03-47ae-a23a-2c47c5ca1044
ms.date: 12/05/2018
ms.keywords: SHEvaluateSystemCommandTemplate, SHEvaluateSystemCommandTemplate function [Windows Shell], _shell_SHEvaluateSystemCommandTemplate, shell.SHEvaluateSystemCommandTemplate, shellapi/SHEvaluateSystemCommandTemplate
req.header: shellapi.h
req.include-header: 
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
req.lib: OneCore.Lib
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHEvaluateSystemCommandTemplate
 - shellapi/SHEvaluateSystemCommandTemplate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell-shell32-l1-5-0.dll
 - ext-ms-win-shell-shell32-l1-4-0.dll
 - ext-ms-win-shell-shell32-l1-3-0.dll
 - ext-ms-win-shell-shell32-l1-2-3.dll
 - Shell32.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
api_name:
 - SHEvaluateSystemCommandTemplate
req.apiset: ext-ms-win-shell-shell32-l1-2-2 (introduced in Windows 10, version 10.0.14393)
---

# SHEvaluateSystemCommandTemplate function


## -description

Enforces strict validation of parameters used in a call to <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a> or <a href="/windows/desktop/api/shellapi/nf-shellapi-shellexecutea">ShellExecute</a>.

## -parameters

### -param pszCmdTemplate [in]

Type: <b>PCWSTR</b>

A command line, which may or may not include parameters. If the parameters are substitution parameters, then <b>SHEvaluateSystemCommandTemplate</b> should be called before parameters have been replaced.

### -param ppszApplication [out]

Type: <b>PWSTR*</b>

A pointer to the verified path to the application. This value should be passed as the <i>lpApplication</i> parameter in a call to <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a> or as the <i>lpFile</i> parameter in a call to <a href="/windows/desktop/api/shellapi/nf-shellapi-shellexecutea">ShellExecute</a>. This resource is allocated using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a>, and it is the responsibility of the caller to free the resource when it is no longer needed by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

### -param ppszCommandLine [out, optional]

Type: <b>PWSTR*</b>

A pointer to a command-line string template to be used in a call to <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>. Command-line parameters should be specified based on this template, and then passed as the <i>lpCommandLine</i> parameter to <b>CreateProcess</b>. It is guaranteed to be of a form that <a href="/windows/desktop/api/shlwapi/nf-shlwapi-pathgetargsa">PathGetArgs</a> can always read correctly. This resource is allocated using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a>, and it is the responsibility of the caller to free the resource when it is no longer needed by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>. 

                    

This parameter can be <b>NULL</b> if this function is not being used in association with a call to <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>.

### -param ppszParameters [out, optional]

Type: <b>PWSTR*</b>

A pointer to a command-line string template to be used in a call to <a href="/windows/desktop/api/shellapi/nf-shellapi-shellexecutea">ShellExecute</a>. Command-line parameters should be specified based on this template, and then passed as the <i>lpParameters</i> parameter to <b>ShellExecute</b>. This parameter is identical to calling <a href="/windows/desktop/api/shlwapi/nf-shlwapi-pathgetargsa">PathGetArgs</a>. This resource is allocated using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a>, and it is the responsibility of the caller to free the resource when it is no longer needed by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>. 

                    

This parameter can be <b>NULL</b> if this function is not being used in association with a call to <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function is used when a calling process needs the deterministic behavior from a command template, regardless of execution context. It ignores the current process state, such as the <code>%PATH%</code>, <a href="/windows/desktop/api/winbase/nf-winbase-getcurrentdirectory">GetCurrentDirectory</a>, and parent process directory.

This function is used when the command is hard-coded.

This function is used by <a href="/windows/desktop/api/shellapi/nf-shellapi-shellexecutea">ShellExecute</a> when handling file associations from HKEY_CLASSES_ROOT. The purpose of this function is to reduce <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a> command-line exploits. It is not designed for processing user input and if used for that purpose can generate unexpected failures.
