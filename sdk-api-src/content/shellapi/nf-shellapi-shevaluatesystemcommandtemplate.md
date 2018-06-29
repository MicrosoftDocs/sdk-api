---
UID: NF:shellapi.SHEvaluateSystemCommandTemplate
title: SHEvaluateSystemCommandTemplate function
author: windows-sdk-content
description: Enforces strict validation of parameters used in a call to CreateProcess or ShellExecute.
old-location: shell\SHEvaluateSystemCommandTemplate.htm
old-project: shell
ms.assetid: 554b941d-7d03-47ae-a23a-2c47c5ca1044
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: SHEvaluateSystemCommandTemplate, SHEvaluateSystemCommandTemplate function [Windows Shell], _shell_SHEvaluateSystemCommandTemplate, shell.SHEvaluateSystemCommandTemplate, shellapi/SHEvaluateSystemCommandTemplate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: SHSTOCKICONID
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
api_name:
 - SHEvaluateSystemCommandTemplate
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Internet Explorer 5.0
---

# SHEvaluateSystemCommandTemplate function


## -description


Enforces strict validation of parameters used in a call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff539321">CreateProcess</a> or <a href="https://msdn.microsoft.com/8b1f3978-a0ee-4684-8a37-98e270b63897">ShellExecute</a>.


## -parameters




### -param pszCmdTemplate [in]

Type: <b>PCWSTR</b>

A command line, which may or may not include parameters. If the parameters are substitution parameters, then <b>SHEvaluateSystemCommandTemplate</b> should be called before parameters have been replaced.


### -param ppszApplication [out]

Type: <b>PWSTR*</b>

A pointer to the verified path to the application. This value should be passed as the <i>lpApplication</i> parameter in a call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff539321">CreateProcess</a> or as the <i>lpFile</i> parameter in a call to <a href="https://msdn.microsoft.com/8b1f3978-a0ee-4684-8a37-98e270b63897">ShellExecute</a>. This resource is allocated using <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a>, and it is the responsibility of the caller to free the resource when it is no longer needed by calling <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.


### -param ppszCommandLine [out, optional]

Type: <b>PWSTR*</b>

A pointer to a command-line string template to be used in a call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff539321">CreateProcess</a>. Command-line parameters should be specified based on this template, and then passed as the <i>lpCommandLine</i> parameter to <b>CreateProcess</b>. It is guaranteed to be of a form that <a href="https://msdn.microsoft.com/17dfb601-1306-41b6-a504-8bf69ff204c9">PathGetArgs</a> can always read correctly. This resource is allocated using <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a>, and it is the responsibility of the caller to free the resource when it is no longer needed by calling <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>. 

                    

This parameter can be <b>NULL</b> if this function is not being used in association with a call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff539321">CreateProcess</a>.


### -param ppszParameters [out, optional]

Type: <b>PWSTR*</b>

A pointer to a command-line string template to be used in a call to <a href="https://msdn.microsoft.com/8b1f3978-a0ee-4684-8a37-98e270b63897">ShellExecute</a>. Command-line parameters should be specified based on this template, and then passed as the <i>lpParameters</i> parameter to <b>ShellExecute</b>. This parameter is identical to calling <a href="https://msdn.microsoft.com/17dfb601-1306-41b6-a504-8bf69ff204c9">PathGetArgs</a>. This resource is allocated using <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a>, and it is the responsibility of the caller to free the resource when it is no longer needed by calling <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>. 

                    

This parameter can be <b>NULL</b> if this function is not being used in association with a call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff539321">CreateProcess</a>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function is used when a calling process needs the deterministic behavior from a command template, regardless of execution context. It ignores the current process state, such as the <code>%PATH%</code>, <a href="https://msdn.microsoft.com/1fbe6289-2ca8-4ca8-b004-ecf513f9b0bd">GetCurrentDirectory</a>, and parent process directory.

This function is used when the command is hard-coded.

This function is used by <a href="https://msdn.microsoft.com/8b1f3978-a0ee-4684-8a37-98e270b63897">ShellExecute</a> when handling file associations from HKEY_CLASSES_ROOT. The purpose of this function is to reduce <a href="https://msdn.microsoft.com/library/windows/hardware/ff539321">CreateProcess</a> command-line exploits. It is not designed for processing user input and if used for that purpose can generate unexpected failures.



