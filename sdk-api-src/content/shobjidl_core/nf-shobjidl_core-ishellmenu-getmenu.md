---
UID: NF:shobjidl_core.IShellMenu.GetMenu
title: IShellMenu::GetMenu (shobjidl_core.h)
description: Gets the menu information set by calling IShellMenu::SetMenu.
helpviewer_keywords: ["GetMenu","GetMenu method [Windows Shell]","GetMenu method [Windows Shell]","IShellMenu interface","IShellMenu interface [Windows Shell]","GetMenu method","IShellMenu.GetMenu","IShellMenu::GetMenu","_shell_IShellMenu_GetMenu","shell.IShellMenu_GetMenu","shobjidl_core/IShellMenu::GetMenu"]
old-location: shell\IShellMenu_GetMenu.htm
tech.root: shell
ms.assetid: b366d9c9-5dd3-43ee-99a1-417b9d907855
ms.date: 12/05/2018
ms.keywords: GetMenu, GetMenu method [Windows Shell], GetMenu method [Windows Shell],IShellMenu interface, IShellMenu interface [Windows Shell],GetMenu method, IShellMenu.GetMenu, IShellMenu::GetMenu, _shell_IShellMenu_GetMenu, shell.IShellMenu_GetMenu, shobjidl_core/IShellMenu::GetMenu
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellMenu::GetMenu
 - shobjidl_core/IShellMenu::GetMenu
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellMenu.GetMenu
---

# IShellMenu::GetMenu


## -description

Gets the menu information set by calling <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenu-setmenu">IShellMenu::SetMenu</a>.

## -parameters

### -param phmenu [out]

Type: <b>HMENU*</b>

When this method returns, contains a pointer to an <b>HMENU</b> value that receives the <i>hmenu</i> value that you specified when you called <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenu-setmenu">IShellMenu::SetMenu</a>. This value can be <b>NULL</b>.

### -param phwnd [out]

Type: <b>HWND*</b>

When this method returns, contains a pointer to an <b>HWND</b> value that receives the <i>hwnd</i> value that you specified when you called <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenu-setmenu">IShellMenu::SetMenu</a>. This value can be <b>NULL</b>.

### -param pdwFlags [out]

Type: <b>DWORD*</b>

When this method returns, contains a pointer to a <b>DWORD</b> value that receives the <i>dwFlags</i> value that you specified when you called <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenu-setmenu">IShellMenu::SetMenu</a>. This value can be <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.