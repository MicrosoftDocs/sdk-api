---
UID: NF:shobjidl_core.GetCurrentProcessExplicitAppUserModelID
title: GetCurrentProcessExplicitAppUserModelID function (shobjidl_core.h)
author: windows-sdk-content
description: Retrieves the application-defined, explicit Application User Model ID (AppUserModelID) for the current process.
old-location: shell\GetCurrentProcessExplicitAppUserModelID.htm
tech.root: shell
ms.assetid: d3af052b-1f58-4c56-914b-a8283aceef5b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetCurrentProcessExplicitAppUserModelID, GetCurrentProcessExplicitAppUserModelID function [Windows Shell], _shell_GetCurrentProcessExplicitAppUserModelID, _shell_GetCurrentProcessExplicitAppUserModelID_cpp, shell.GetCurrentProcessExplicitAppUserModelID, shobjidl_core/GetCurrentProcessExplicitAppUserModelID
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
 - GetCurrentProcessExplicitAppUserModelID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetCurrentProcessExplicitAppUserModelID function


## -description


Retrieves the application-defined, explicit Application User Model ID (AppUserModelID) for the current process.


## -parameters




### -param AppID [out]

Type: <b>PWSTR*</b>

A pointer that receives the address of the AppUserModelID assigned to the process. The caller is responsible for freeing this string with <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> when it is no longer needed.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The AppUserModelID retrieved by this function was set earlier through <a href="https://msdn.microsoft.com/2b8baf6d-9c9a-4727-9deb-3d335bd0dc7c">SetCurrentProcessExplicitAppUserModelID</a>.

An application can only retrieve an AppUserModelID that has been explicitly set. System-assigned default AppUserModelIDs cannot be retrieved. If the application requires knowledge of its AppUserModelID it should set one explicitly.




## -see-also




<a href="https://msdn.microsoft.com/ebce2d99-6f20-4545-9f12-d79cd8d0828f">Application User Model IDs (AppUserModelIDs)</a>



<a href="https://msdn.microsoft.com/da6c4799-fda9-43e5-86eb-91a40db5ab6c">IObjectWithAppUserModelID::GetAppID</a>



<a href="https://msdn.microsoft.com/cbf2b07d-d67c-4755-888c-d40692d13cae">Taskbar Extensions</a>
 

 

