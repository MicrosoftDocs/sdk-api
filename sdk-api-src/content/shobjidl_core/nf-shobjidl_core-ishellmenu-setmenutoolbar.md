---
UID: NF:shobjidl_core.IShellMenu.SetMenuToolbar
title: IShellMenu::SetMenuToolbar (shobjidl_core.h)
description: Adds a menu to the menuband.
old-location: shell\IShellMenu_SetMenuToolbar.htm
tech.root: shell
ms.assetid: 6067f2be-883a-4271-95ad-16fd868b37a0
ms.date: 12/05/2018
ms.keywords: IShellMenu interface [Windows Shell],SetMenuToolbar method, IShellMenu.SetMenuToolbar, IShellMenu::SetMenuToolbar, SMSET_BOTTOM, SMSET_DONTOWN, SMSET_TOP, SetMenuToolbar, SetMenuToolbar method [Windows Shell], SetMenuToolbar method [Windows Shell],IShellMenu interface, _shell_IShellMenu_SetMenuToolbar, shell.IShellMenu_SetMenuToolbar, shobjidl_core/IShellMenu::SetMenuToolbar
f1_keywords:
- shobjidl_core/IShellMenu.SetMenuToolbar
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Shell32.dll
api_name:
- IShellMenu.SetMenuToolbar
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IShellMenu::SetMenuToolbar


## -description


Adds a menu to the menuband.


## -parameters




### -param punk [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to an object that supports <b>CLSID_MenuToolbarBase</b> in its <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> method.


### -param dwFlags [in]

Type: <b>DWORD</b>

Flags that control how the menu operates.



#### SMSET_TOP

Bias this namespace to the top of the menu.




#### SMSET_BOTTOM

Bias this namespace to the bottom of the menu.



#### SMSET_DONTOWN

The Menuband does not own the non-ref counted object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



