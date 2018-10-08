---
UID: NF:shlobj_core.SHGetSpecialFolderLocation
title: SHGetSpecialFolderLocation function
author: windows-sdk-content
description: SHGetSpecialFolderLocation is not supported and may be altered or unavailable in the future. Instead, use SHGetFolderLocation.
old-location: shell\SHGetSpecialFolderLocation.htm
tech.root: shell
ms.assetid: 10b00497-fc3b-4e34-acd8-bc0721c0dc05
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: SHGetSpecialFolderLocation, SHGetSpecialFolderLocation function [Windows Shell], _win32_SHGetSpecialFolderLocation, _win32_SHGetSpecialFolderLocation_cpp, shell.SHGetSpecialFolderLocation, shlobj_core/SHGetSpecialFolderLocation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.lib: Shell32.lib
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - API-MS-Win-Storage-Exports-Internal-L1-1-0.dll
 - Windows.Storage.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
api_name:
 - SHGetSpecialFolderLocation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SHGetSpecialFolderLocation function


## -description


<p class="CCE_Message">[<b>SHGetSpecialFolderLocation</b> is not supported and may be altered or unavailable in the future. Instead, use <a href="https://msdn.microsoft.com/6fcac066-1ab0-443a-9994-b68ead3bbc20">SHGetFolderLocation</a>.]

Retrieves a pointer to the <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure of a special folder.


## -parameters




### -param hwnd [in]

Type: <b>HWND</b>

Reserved.


### -param csidl [in]

Type: <b>int</b>

A <a href="https://msdn.microsoft.com/33d92271-2865-4ebd-b96c-bf293deb4310">CSIDL</a> value that identifies the folder of interest.


### -param ppidl [out]

Type: <b>PIDLIST_ABSOLUTE*</b>

A PIDL specifying the folder's location relative to the root of the namespace (the desktop). It is the responsibility of the calling application to free the returned IDList by using <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/4c39fdc1-5e43-4042-8703-fb72c88e2637">SHGetSpecialFolderPath</a>
 

 

