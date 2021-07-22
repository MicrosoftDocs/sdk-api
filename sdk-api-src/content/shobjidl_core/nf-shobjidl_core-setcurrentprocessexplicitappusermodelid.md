---
UID: NF:shobjidl_core.SetCurrentProcessExplicitAppUserModelID
title: SetCurrentProcessExplicitAppUserModelID function (shobjidl_core.h)
description: Specifies a unique application-defined Application User Model ID (AppUserModelID) that identifies the current process to the taskbar. This identifier allows an application to group its associated processes and windows under a single taskbar button.
helpviewer_keywords: ["SetCurrentProcessExplicitAppUserModelID","SetCurrentProcessExplicitAppUserModelID function [Windows Shell]","_shell_SetCurrentProcessExplicitAppUserModelID","shell.SetCurrentProcessExplicitAppUserModelID","shobjidl_core/SetCurrentProcessExplicitAppUserModelID"]
old-location: shell\SetCurrentProcessExplicitAppUserModelID.htm
tech.root: shell
ms.assetid: 2b8baf6d-9c9a-4727-9deb-3d335bd0dc7c
ms.date: 12/05/2018
ms.keywords: SetCurrentProcessExplicitAppUserModelID, SetCurrentProcessExplicitAppUserModelID function [Windows Shell], _shell_SetCurrentProcessExplicitAppUserModelID, shell.SetCurrentProcessExplicitAppUserModelID, shobjidl_core/SetCurrentProcessExplicitAppUserModelID
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
 - SetCurrentProcessExplicitAppUserModelID
 - shobjidl_core/SetCurrentProcessExplicitAppUserModelID
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
 - SetCurrentProcessExplicitAppUserModelID
---

# SetCurrentProcessExplicitAppUserModelID function


## -description

Specifies a unique application-defined Application User Model ID (AppUserModelID) that identifies the current process to the taskbar. This identifier allows an application to group its associated processes and windows under a single taskbar button.

## -parameters

### -param AppID [in]

Type: <b>PCWSTR</b>

Pointer to the AppUserModelID to assign to the current process.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method must be called during an application's initial startup routine before the application presents any UI or makes any manipulation of its Jump Lists. This includes any call to <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs">SHAddToRecentDocs</a>.

## -see-also

<a href="/windows/desktop/shell/appids">Application User Model IDs (AppUserModelIDs)</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-getcurrentprocessexplicitappusermodelid">GetCurrentProcessExplicitAppUserModelID</a>



<a href="/windows/desktop/shell/taskbar-extensions">Taskbar Extensions</a>