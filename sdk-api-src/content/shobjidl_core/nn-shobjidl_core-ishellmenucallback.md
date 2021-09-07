---
UID: NN:shobjidl_core.IShellMenuCallback
title: IShellMenuCallback (shobjidl_core.h)
description: A callback interface that exposes a method that receives messages from a menu band.
helpviewer_keywords: ["IShellMenuCallback","IShellMenuCallback interface [Windows Shell]","IShellMenuCallback interface [Windows Shell]","described","_win32_IShellMenuCallback","shell.IShellMenuCallback","shobjidl_core/IShellMenuCallback"]
old-location: shell\IShellMenuCallback.htm
tech.root: shell
ms.assetid: 96bfdc52-bd4a-4345-8dd1-7e716a3d9811
ms.date: 12/05/2018
ms.keywords: IShellMenuCallback, IShellMenuCallback interface [Windows Shell], IShellMenuCallback interface [Windows Shell],described, _win32_IShellMenuCallback, shell.IShellMenuCallback, shobjidl_core/IShellMenuCallback
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellMenuCallback
 - shobjidl_core/IShellMenuCallback
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
 - IShellMenuCallback
---

# IShellMenuCallback interface


## -description

A callback interface that exposes a method that receives messages from a menu band.

## -inheritance

The <b>IShellMenuCallback</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IShellMenuCallback</b> also has these types of members:

## -remarks

Once you have created the menu band object, pass a pointer to this interface to the menu band object by calling <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenu-initialize">IShellMenu::Initialize</a>. You receive messages from the menu band through the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm">IShellMenuCallback::CallbackSM</a> method.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imenuband">IMenuBand</a>



<a href="/windows/desktop/shell/profiles-directory">MenuBand</a>
