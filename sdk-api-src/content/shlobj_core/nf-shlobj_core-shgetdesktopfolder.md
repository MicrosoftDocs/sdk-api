---
UID: NF:shlobj_core.SHGetDesktopFolder
title: SHGetDesktopFolder function
author: windows-sdk-content
description: Retrieves the IShellFolder interface for the desktop folder, which is the root of the Shell's namespace.
old-location: shell\SHGetDesktopFolder.htm
tech.root: shell
ms.assetid: 121cbd41-d512-4f33-b89c-d0dd9933df87
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: SHGetDesktopFolder, SHGetDesktopFolder function [Windows Shell], _win32_SHGetDesktopFolder, shell.SHGetDesktopFolder, shlobj_core/SHGetDesktopFolder
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
 - API-MS-Win-shell-shellfolders-l1-1-0.dll
 - KernelBase.dll
 - Ext-MS-Win-Shell32-Shellfolders-L1-1-0.dll
 - Ext-MS-Win-Shell32-Shellfolders-L1-1-1.dll
 - Windows.Storage.dll
api_name:
 - SHGetDesktopFolder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SHGetDesktopFolder function


## -description


Retrieves the <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a> interface for the desktop folder, which is the root of the Shell's namespace.


## -parameters




### -param ppshf [out]

Type: <b><a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a>**</b>

When this method returns, receives an <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a> interface pointer for the desktop folder. The calling application is responsible for eventually freeing the interface by calling its <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> method.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



