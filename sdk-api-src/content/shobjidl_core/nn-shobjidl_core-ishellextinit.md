---
UID: NN:shobjidl_core.IShellExtInit
title: IShellExtInit (shobjidl_core.h)
description: Exposes a method that initializes Shell extensions for property sheets, shortcut menus, and drag-and-drop handlers (extensions that add items to shortcut menus during nondefault drag-and-drop operations).
helpviewer_keywords: ["IShellExtInit","IShellExtInit interface [Windows Shell]","IShellExtInit interface [Windows Shell]","described","_win32_IShellExtInit","_win32_ishellextinit_cpp","shell.IShellExtInit","shobjidl_core/IShellExtInit"]
old-location: shell\IShellExtInit.htm
tech.root: shell
ms.assetid: 5f7e7f71-4cd6-4ce4-946c-9a1f7ec72fbe
ms.date: 12/05/2018
ms.keywords: IShellExtInit, IShellExtInit interface [Windows Shell], IShellExtInit interface [Windows Shell],described, _win32_IShellExtInit, _win32_ishellextinit_cpp, shell.IShellExtInit, shobjidl_core/IShellExtInit
req.header: shobjidl_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl_core.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellExtInit
 - shobjidl_core/IShellExtInit
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
 - IShellExtInit
---

# IShellExtInit interface


## -description

Exposes a method that initializes Shell extensions for property sheets, shortcut menus, and drag-and-drop handlers (extensions that add items to shortcut menus during nondefault drag-and-drop operations).

## -inheritance

The <b>IShellExtInit</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IShellExtInit</b> also has these types of members:

## -remarks

Implement <b>IShellExtInit</b> when you are writing a handler based on the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu">IContextMenu</a> or <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext">IShellPropSheetExt</a> interface.

Note that Shell extensions based on other interfaces do not use this method of initialization.

You do not use this interface directly. The Shell calls it to initialize the handler.
