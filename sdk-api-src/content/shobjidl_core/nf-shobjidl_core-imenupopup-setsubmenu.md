---
UID: NF:shobjidl_core.IMenuPopup.SetSubMenu
title: IMenuPopup::SetSubMenu (shobjidl_core.h)
description: Sets the given menu bar interface to be the submenu of the calling application object's interface.
helpviewer_keywords: ["IMenuPopup interface [Windows Shell]","SetSubMenu method","IMenuPopup.SetSubMenu","IMenuPopup::SetSubMenu","SetSubMenu","SetSubMenu method [Windows Shell]","SetSubMenu method [Windows Shell]","IMenuPopup interface","_win32_IMenuPopup_SetSubMenu","shell.IMenuPopup_SetSubMenu","shobjidl_core/IMenuPopup::SetSubMenu"]
old-location: shell\IMenuPopup_SetSubMenu.htm
tech.root: shell
ms.assetid: c2f80502-bac5-4a6f-95ba-1610c548e636
ms.date: 12/05/2018
ms.keywords: IMenuPopup interface [Windows Shell],SetSubMenu method, IMenuPopup.SetSubMenu, IMenuPopup::SetSubMenu, SetSubMenu, SetSubMenu method [Windows Shell], SetSubMenu method [Windows Shell],IMenuPopup interface, _win32_IMenuPopup_SetSubMenu, shell.IMenuPopup_SetSubMenu, shobjidl_core/IMenuPopup::SetSubMenu
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMenuPopup::SetSubMenu
 - shobjidl_core/IMenuPopup::SetSubMenu
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IMenuPopup.SetSubMenu
---

# IMenuPopup::SetSubMenu


## -description

Sets the given menu bar interface to be the submenu of the calling application object's interface.

## -parameters

### -param pmp [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imenupopup">IMenuPopup</a>*</b>

A pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imenupopup">IMenuPopup</a> interface that specifies the menu bar of interest.

### -param fSet

Type: <b>BOOL</b>

Removes the submenu if <i>fSet</i> is set to <b>FALSE</b>.

## -returns

Type: <b>HRESULT</b>

Always returns S_OK.