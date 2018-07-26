---
UID: NF:shlobj_core.SHGetSpecialFolderPathA
title: SHGetSpecialFolderPathA function
author: windows-sdk-content
description: SHGetSpecialFolderPath is not supported. Instead, use ShGetFolderPath.
old-location: shell\SHGetSpecialFolderPath.htm
old-project: shell
ms.assetid: 4c39fdc1-5e43-4042-8703-fb72c88e2637
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: SHGetSpecialFolderPath, SHGetSpecialFolderPath function [Windows Shell], SHGetSpecialFolderPathA, SHGetSpecialFolderPathW, _win32_SHGetSpecialFolderPath, shell.SHGetSpecialFolderPath, shlobj_core/SHGetSpecialFolderPath, shlobj_core/SHGetSpecialFolderPathA, shlobj_core/SHGetSpecialFolderPathW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shlobj_core.h
req.include-header: Shlobj.h, Shlobj_core.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHGetSpecialFolderPathW (Unicode) and SHGetSpecialFolderPathA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: AUTOCOMPLETELISTOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
 - API-MS-Win-shell-shellfolders-l1-1-0.dll
 - KernelBase.dll
 - Ext-MS-Win-Shell32-Shellfolders-L1-1-0.dll
 - Ext-MS-Win-Shell32-Shellfolders-L1-1-1.dll
 - Windows.Storage.dll
api_name:
 - SHGetSpecialFolderPath
 - SHGetSpecialFolderPathA
 - SHGetSpecialFolderPathW
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# SHGetSpecialFolderPathA function


## -description


<p class="CCE_Message">[<b>SHGetSpecialFolderPath</b> is not supported. Instead, use <a href="https://msdn.microsoft.com/a240abc0-e0a6-4f95-8e74-7dc410970212">ShGetFolderPath</a>.]

Retrieves the path of a special folder, identified by its <a href="https://msdn.microsoft.com/33d92271-2865-4ebd-b96c-bf293deb4310">CSIDL</a>.


## -parameters




### -param hwnd

TBD


### -param pszPath

TBD


### -param csidl [in]

Type: <b>int</b>

A <a href="https://msdn.microsoft.com/33d92271-2865-4ebd-b96c-bf293deb4310">CSIDL</a> that identifies the folder of interest. If a virtual folder is specified, this function will fail.


### -param fCreate [in]

Type: <b>BOOL</b>

Indicates whether the folder should be created if it does not already exist. If this value is nonzero, the folder is created. If this value is zero, the folder is not created.


#### - hwndOwner

Type: <b>HWND</b>

Reserved.


#### - lpszPath [out]

Type: <b>LPTSTR</b>

A pointer to a null-terminated string that receives the drive and path of the specified folder. This buffer must be at least MAX_PATH characters in size.


## -returns



Type: <b>BOOL</b>

<b>TRUE</b> if successful; otherwise, <b>FALSE</b>.




## -remarks



The Microsoft Internet Explorer 4.0 Desktop Update must be installed for this function to be available.



