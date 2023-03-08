---
UID: NF:shobjidl_core.IShellMenu.SetMenu
title: IShellMenu::SetMenu (shobjidl_core.h)
description: Appends a static menu to the menu band.
helpviewer_keywords: ["IShellMenu interface [Windows Shell]","SetMenu method","IShellMenu.SetMenu","IShellMenu::SetMenu","SMSET_BOTTOM","SMSET_DONTOWN","SMSET_TOP","SetMenu","SetMenu method [Windows Shell]","SetMenu method [Windows Shell]","IShellMenu interface","_shell_IShellMenu_SetMenu","shell.IShellMenu_SetMenu","shobjidl_core/IShellMenu::SetMenu"]
old-location: shell\IShellMenu_SetMenu.htm
tech.root: shell
ms.assetid: afa393eb-05a0-478e-88a2-7c31b4a48930
ms.date: 12/05/2018
ms.keywords: IShellMenu interface [Windows Shell],SetMenu method, IShellMenu.SetMenu, IShellMenu::SetMenu, SMSET_BOTTOM, SMSET_DONTOWN, SMSET_TOP, SetMenu, SetMenu method [Windows Shell], SetMenu method [Windows Shell],IShellMenu interface, _shell_IShellMenu_SetMenu, shell.IShellMenu_SetMenu, shobjidl_core/IShellMenu::SetMenu
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
 - IShellMenu::SetMenu
 - shobjidl_core/IShellMenu::SetMenu
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
 - IShellMenu.SetMenu
---

# IShellMenu::SetMenu


## -description

Appends a static menu to the menu band.

## -parameters

### -param hmenu [in]

Type: <b>HMENU</b>

The handle of the static menu that is to be appended. This value can be <b>NULL</b>.

### -param hwnd [in]

Type: <b>HWND</b>

The <b>HWND</b> of the owner window. This value can be <b>NULL</b>.

### -param dwFlags [in]

Type: <b>DWORD</b>

Flags that specify how the menu operates.



#### SMSET_BOTTOM

Attach the menu to the bottom of the parent menu.



#### SMSET_TOP

Attach the menu to the top of the parent menu.



#### SMSET_DONTOWN

The menu band does not own the menu named in <i>hwnd</i>, so should that menu eventually be replaced, it should not be destroyed.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

