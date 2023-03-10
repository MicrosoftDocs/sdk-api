---
UID: NF:shlwapi.DllInstall
title: DllInstall function (shlwapi.h)
description: Handles installation and setup for a DLL.
helpviewer_keywords: ["DllInstall","DllInstall function [Windows Shell]","_win32_DllInstall","shell.DllInstall","shlwapi/DllInstall"]
old-location: shell\DllInstall.htm
tech.root: shell
ms.assetid: d161f2ec-31e6-405e-b76c-9976b0880816
ms.date: 12/05/2018
ms.keywords: DllInstall, DllInstall function [Windows Shell], _win32_DllInstall, shell.DllInstall, shlwapi/DllInstall
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shlwapi.dll (version 4.71 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DllInstall
 - shlwapi/DllInstall
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
api_name:
 - DllInstall
---

# DllInstall function


## -description

Handles installation and setup for a DLL.

## -parameters

### -param bInstall

Type: <b>BOOL</b>

<b>TRUE</b> if the DLL is being installed; <b>FALSE</b> if it is being uninstalled.

### -param pszCmdLine [in, optional]

Type: <b>PCWSTR</b>

A string passed in by <b>regsvr32</b> that indicates which setup procedure to use. This value can be <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function may be implemented and exported by name by a DLL for use during application installation or setup. It is invoked by <b>regsvr32</b> to allow the DLL to perform tasks such as adding information to the registry.

<b>DllInstall</b> is used only for application installation and setup. It should not be called by an application. It is similar in purpose to <a href="/windows/desktop/api/olectl/nf-olectl-dllregisterserver">DllRegisterServer</a> or <a href="/windows/desktop/api/olectl/nf-olectl-dllunregisterserver">DllUnregisterServer</a>. Unlike these functions, <b>DllInstall</b> takes an input string which can be used to specify a variety of different actions. This allows a DLL to be installed in more than one way, based on any criteria that is appropriate.

To use <b>DllInstall</b> with <b>regsvr32</b>, add a "/i" flag followed by a colon (:) and a string. The string will be passed to <b>DllInstall</b> as the <i>pszCmdLine</i> parameter. If you omit the colon and string, <i>pszCmdLine</i> will be set to <b>NULL</b>. The following example would be used to install a DLL.

<b>regsvr32 /i:"Install_1" dllname.dll</b>

<b>DllInstall</b> is invoked with <i>bInstall</i> set to <b>TRUE</b> and <i>pszCmdLine</i> set to "Install_1". To uninstall a DLL, use the following:

<b>regsvr32 /u /i:"Install_1" dllname.dll</b>

With both of the above examples, <a href="/windows/desktop/api/olectl/nf-olectl-dllregisterserver">DllRegisterServer</a> or <a href="/windows/desktop/api/olectl/nf-olectl-dllunregisterserver">DllUnregisterServer</a> will also be called. To call <b>DllInstall</b> only, add a "/n" flag.

<b>regsvr32 /n /i:"Install_1" dllname.dll</b>