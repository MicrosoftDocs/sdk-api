---
UID: NN:shobjidl_core.IShellMenu
title: IShellMenu (shobjidl_core.h)
description: Exposes methods that interact with Shell menus such as the Start menu, and the Favorites menu.
helpviewer_keywords: ["IShellMenu","IShellMenu interface [Windows Shell]","IShellMenu interface [Windows Shell]","described","_shell_IShellMenu","shell.IShellMenu","shobjidl_core/IShellMenu"]
old-location: shell\IShellMenu.htm
tech.root: shell
ms.assetid: 46793ae9-936e-4a58-bc34-84396151b4a3
ms.date: 12/05/2018
ms.keywords: IShellMenu, IShellMenu interface [Windows Shell], IShellMenu interface [Windows Shell],described, _shell_IShellMenu, shell.IShellMenu, shobjidl_core/IShellMenu
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
 - IShellMenu
 - shobjidl_core/IShellMenu
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
 - IShellMenu
---

# IShellMenu interface


## -description

Exposes methods that interact with Shell menus such as the <b>Start</b> menu, and the <b>Favorites</b> menu.

## -inheritance

The <b>IShellMenu</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IShellMenu</b> also has these types of members:

## -remarks

To get a pointer to this interface, call <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> with the <i>rclsid</i> parameter set to CLSID_MenuBand and the <i>riid</i> parameter set to IID_IShellMenu. You must first initialize the interface by calling <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenu-initialize">IShellMenu::Initialize</a>, and then initialize the menu band by calling <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenu-setshellfolder">IShellMenu::SetShellFolder</a>.
