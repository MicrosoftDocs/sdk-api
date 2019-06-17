---
UID: NF:shlobj_core.SHCreateDefaultContextMenu
title: SHCreateDefaultContextMenu function (shlobj_core.h)
author: windows-sdk-content
description: Creates an object that represents the Shell's default context menu implementation.
old-location: shell\SHCreateDefaultContextMenu.htm
tech.root: shell
ms.assetid: 055ff0a0-9ba7-463d-9684-3fd072b190da
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SHCreateDefaultContextMenu, SHCreateDefaultContextMenu function [Windows Shell], _shell_SHCreateDefaultContextMenu, shell.SHCreateDefaultContextMenu, shlobj_core/SHCreateDefaultContextMenu
ms.topic: function
f1_keywords: ["shlobj_core/SHCreateDefaultContextMenu"]
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Shell32.dll (version 6.0.6000 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHCreateDefaultContextMenu
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SHCreateDefaultContextMenu function


## -description


Creates an object that represents the Shell's default context menu implementation.


## -parameters




### -param pdcm [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/ns-shlobj_core-defcontextmenu">DEFCONTEXTMENU</a>*</b>

A pointer to a constant <a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/ns-shlobj_core-defcontextmenu">DEFCONTEXTMENU</a> structure.


### -param riid

Type: <b>REFIID</b>

Reference to the interface ID of the interface on which to base the object. This is typically the IID of <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu">IContextMenu</a>, <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2">IContextMenu2</a>, or <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3">IContextMenu3</a>.


### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the interface pointer requested in <i>riid</i>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function is typically used in the implementation of <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof">IShellFolder::GetUIObjectOf</a>. <b>GetUIObjectOf</b> creates a context menu that merges <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu">IContextMenu</a> handlers specified by the <a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/ns-shlobj_core-defcontextmenu">DEFCONTEXTMENU</a> structure, and can optionally provide default context menu verb implementations such as open, explore, delete, and copy.

The operation of this function is controlled by the input specified in the <a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/ns-shlobj_core-defcontextmenu">DEFCONTEXTMENU</a> structure.The API<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2">CDefFolderMenu_Create2</a> is another way to construct the default context menu implementation. It is less expressive than <b>SHCreateDefaultContextMenu</b> but it exists in platforms prior to Windows Vista.
           



