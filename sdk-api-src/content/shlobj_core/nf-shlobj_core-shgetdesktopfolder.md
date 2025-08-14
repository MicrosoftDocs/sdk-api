---
UID: NF:shlobj_core.SHGetDesktopFolder
title: SHGetDesktopFolder function (shlobj_core.h)
description: Retrieves the IShellFolder interface for the desktop folder, which is the root of the Shell's namespace.
helpviewer_keywords: ["SHGetDesktopFolder","SHGetDesktopFolder function [Windows Shell]","_win32_SHGetDesktopFolder","shell.SHGetDesktopFolder","shlobj_core/SHGetDesktopFolder"]
old-location: shell\SHGetDesktopFolder.htm
tech.root: shell
ms.assetid: 121cbd41-d512-4f33-b89c-d0dd9933df87
ms.date: 12/05/2018
ms.keywords: SHGetDesktopFolder, SHGetDesktopFolder function [Windows Shell], _win32_SHGetDesktopFolder, shell.SHGetDesktopFolder, shlobj_core/SHGetDesktopFolder
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHGetDesktopFolder
 - shlobj_core/SHGetDesktopFolder
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell32-shellfolders-l1-2-1.dll
 - ext-ms-win-shell32-shellfolders-l1-2-0.dll
 - api-ms-win-shell-shellfolders-l1-1-1.dll
 - Shell32.dll
 - API-MS-Win-shell-shellfolders-l1-1-0.dll
 - KernelBase.dll
 - Ext-MS-Win-Shell32-Shellfolders-L1-1-0.dll
 - Ext-MS-Win-Shell32-Shellfolders-L1-1-1.dll
 - Windows.Storage.dll
api_name:
 - SHGetDesktopFolder
---

# SHGetDesktopFolder function


## -description

Retrieves the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> interface for the desktop folder, which is the root of the Shell's namespace.

## -parameters

### -param ppshf [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>**</b>

When this method returns, receives an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> interface pointer for the desktop folder. The calling application is responsible for eventually freeing the interface by calling its <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.