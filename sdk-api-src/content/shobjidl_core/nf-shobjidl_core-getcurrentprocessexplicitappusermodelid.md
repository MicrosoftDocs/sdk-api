---
UID: NF:shobjidl_core.GetCurrentProcessExplicitAppUserModelID
title: GetCurrentProcessExplicitAppUserModelID function (shobjidl_core.h)
description: Retrieves the application-defined, explicit Application User Model ID (AppUserModelID) for the current process.
helpviewer_keywords: ["GetCurrentProcessExplicitAppUserModelID","GetCurrentProcessExplicitAppUserModelID function [Windows Shell]","_shell_GetCurrentProcessExplicitAppUserModelID","_shell_GetCurrentProcessExplicitAppUserModelID_cpp","shell.GetCurrentProcessExplicitAppUserModelID","shobjidl_core/GetCurrentProcessExplicitAppUserModelID"]
old-location: shell\GetCurrentProcessExplicitAppUserModelID.htm
tech.root: shell
ms.assetid: d3af052b-1f58-4c56-914b-a8283aceef5b
ms.date: 12/05/2018
ms.keywords: GetCurrentProcessExplicitAppUserModelID, GetCurrentProcessExplicitAppUserModelID function [Windows Shell], _shell_GetCurrentProcessExplicitAppUserModelID, _shell_GetCurrentProcessExplicitAppUserModelID_cpp, shell.GetCurrentProcessExplicitAppUserModelID, shobjidl_core/GetCurrentProcessExplicitAppUserModelID
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.1 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetCurrentProcessExplicitAppUserModelID
 - shobjidl_core/GetCurrentProcessExplicitAppUserModelID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
 - API-MS-Win-DownLevel-shell32-l1-1-0.dll
 - ShCore.dll
 - API-MS-Win-ShCore-SysInfo-l1-1-0.dll
api_name:
 - GetCurrentProcessExplicitAppUserModelID
---

# GetCurrentProcessExplicitAppUserModelID function


## -description

Retrieves the application-defined, explicit Application User Model ID (AppUserModelID) for the current process.

## -parameters

### -param AppID [out]

Type: <b>PWSTR*</b>

A pointer that receives the address of the AppUserModelID assigned to the process. The caller is responsible for freeing this string with <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> when it is no longer needed.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The AppUserModelID retrieved by this function was set earlier through <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-setcurrentprocessexplicitappusermodelid">SetCurrentProcessExplicitAppUserModelID</a>.

An application can only retrieve an AppUserModelID that has been explicitly set. System-assigned default AppUserModelIDs cannot be retrieved. If the application requires knowledge of its AppUserModelID it should set one explicitly.

## -see-also

<a href="/windows/desktop/shell/appids">Application User Model IDs (AppUserModelIDs)</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iobjectwithappusermodelid-getappid">IObjectWithAppUserModelID::GetAppID</a>



<a href="/windows/desktop/shell/taskbar-extensions">Taskbar Extensions</a>