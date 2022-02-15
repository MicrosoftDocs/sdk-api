---
UID: NF:shobjidl_core.IShellMenu.InvalidateItem
title: IShellMenu::InvalidateItem (shobjidl_core.h)
description: Redraws an item in a menu band.
helpviewer_keywords: ["IShellMenu interface [Windows Shell]","InvalidateItem method","IShellMenu.InvalidateItem","IShellMenu::InvalidateItem","InvalidateItem","InvalidateItem method [Windows Shell]","InvalidateItem method [Windows Shell]","IShellMenu interface","_shell_IShellMenu_InvalidateItem","shell.IShellMenu_InvalidateItem","shobjidl_core/IShellMenu::InvalidateItem"]
old-location: shell\IShellMenu_InvalidateItem.htm
tech.root: shell
ms.assetid: 694722f2-2030-4c85-bcc4-70f8a8b70161
ms.date: 12/05/2018
ms.keywords: IShellMenu interface [Windows Shell],InvalidateItem method, IShellMenu.InvalidateItem, IShellMenu::InvalidateItem, InvalidateItem, InvalidateItem method [Windows Shell], InvalidateItem method [Windows Shell],IShellMenu interface, _shell_IShellMenu_InvalidateItem, shell.IShellMenu_InvalidateItem, shobjidl_core/IShellMenu::InvalidateItem
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
 - IShellMenu::InvalidateItem
 - shobjidl_core/IShellMenu::InvalidateItem
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
 - IShellMenu.InvalidateItem
---

# IShellMenu::InvalidateItem


## -description

Redraws an item in a menu band.

## -parameters

### -param psmd [in]

Type: <b>LPSMDATA</b>

A pointer to an <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-smdata">SMDATA</a> structure that identifies the item to be redrawn. Set this value to <b>NULL</b> to redraw the entire menu.

### -param dwFlags [in]

Type: <b>DWORD</b>

Flags that control how the menu is redrawn. If <i>psmd</i> is <b>NULL</b>, set <i>dwFlags</i> to SMINV_REFRESH. If <i>psmd</i> is set to a valid <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-smdata">SMDATA</a> structure, set <i>dwFlags</i> to SMINV_ID | SMINV_REFRESH.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.