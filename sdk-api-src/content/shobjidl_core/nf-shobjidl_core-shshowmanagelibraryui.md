---
UID: NF:shobjidl_core.SHShowManageLibraryUI
title: SHShowManageLibraryUI function (shobjidl_core.h)
description: Shows the library management dialog box, which enables users to manage the library folders and default save location.
helpviewer_keywords: ["SHShowManageLibraryUI","SHShowManageLibraryUI function [Windows Shell]","_shell_SHShowManageLibraryUI","shell.SHShowManageLibraryUI","shobjidl_core/SHShowManageLibraryUI"]
old-location: shell\SHShowManageLibraryUI.htm
tech.root: shell
ms.assetid: 1ac911bb-28d6-4cb6-a66a-1a0c8a4bd6a1
ms.date: 12/05/2018
ms.keywords: SHShowManageLibraryUI, SHShowManageLibraryUI function [Windows Shell], _shell_SHShowManageLibraryUI, shell.SHShowManageLibraryUI, shobjidl_core/SHShowManageLibraryUI
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
req.lib: OneCore.Lib
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHShowManageLibraryUI
 - shobjidl_core/SHShowManageLibraryUI
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHShowManageLibraryUI
---

# SHShowManageLibraryUI function


## -description

Shows the library management dialog box, which enables users to manage the library folders and default save location.

## -parameters

### -param psiLibrary [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> object that represents the library that is to be managed.

### -param hwndOwner [in, optional]

Type: <b>HWND</b>

The handle for the window that owns the library management dialog box. The value of this parameter can be <b>NULL</b>.

### -param pszTitle [in, optional]

Type: <b>LPCWSTR</b>

A pointer to the title for the library management dialog. To display the generic title string, set the value of this parameter to <b>NULL</b>.

### -param pszInstruction [in, optional]

Type: <b>LPCWSTR</b>

A pointer to a help string to display below the title string in the library management dialog box. To display the generic help string, set the value of this parameter to <b>NULL</b>.

### -param lmdOptions [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-librarymanagedialogoptions">LIBRARYMANAGEDIALOGOPTIONS</a></b>

A value from the <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-librarymanagedialogoptions">LIBRARYMANAGEDIALOGOPTIONS</a> enumeration that specifies the behavior of the management dialog box.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a>



<a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-librarymanagedialogoptions">LIBRARYMANAGEDIALOGOPTIONS</a>