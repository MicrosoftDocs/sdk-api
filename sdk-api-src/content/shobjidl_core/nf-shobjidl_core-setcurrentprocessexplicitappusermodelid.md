---
UID: NF:shobjidl_core.SetCurrentProcessExplicitAppUserModelID
title: SetCurrentProcessExplicitAppUserModelID function (shobjidl_core.h)
author: windows-sdk-content
description: Specifies a unique application-defined Application User Model ID (AppUserModelID) that identifies the current process to the taskbar. This identifier allows an application to group its associated processes and windows under a single taskbar button.
old-location: shell\SetCurrentProcessExplicitAppUserModelID.htm
tech.root: shell
ms.assetid: 2b8baf6d-9c9a-4727-9deb-3d335bd0dc7c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SetCurrentProcessExplicitAppUserModelID, SetCurrentProcessExplicitAppUserModelID function [Windows Shell], _shell_SetCurrentProcessExplicitAppUserModelID, shell.SetCurrentProcessExplicitAppUserModelID, shobjidl_core/SetCurrentProcessExplicitAppUserModelID
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method must be called during an application's initial startup routine before the application presents any UI or makes any manipulation of its Jump Lists. This includes any call to <a href="https://msdn.microsoft.com/84e065e6-b68d-4303-b98b-3f8507539468">SHAddToRecentDocs</a>.




## -see-also




<a href="https://msdn.microsoft.com/ebce2d99-6f20-4545-9f12-d79cd8d0828f">Application User Model IDs (AppUserModelIDs)</a>



<a href="https://msdn.microsoft.com/d3af052b-1f58-4c56-914b-a8283aceef5b">GetCurrentProcessExplicitAppUserModelID</a>



<a href="https://msdn.microsoft.com/cbf2b07d-d67c-4755-888c-d40692d13cae">Taskbar Extensions</a>
 

 

