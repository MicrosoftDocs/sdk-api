---
UID: NN:shobjidl_core.IContextMenuCB
title: IContextMenuCB (shobjidl_core.h)
description: Exposes a method that enables the callback of a context menu. For example, to add a shield icon to a menuItem that requires elevation.
helpviewer_keywords: ["IContextMenuCB","IContextMenuCB interface [Windows Shell]","IContextMenuCB interface [Windows Shell]","described","_shell_IContextMenuCB","shell.IContextMenuCB","shobjidl_core/IContextMenuCB"]
old-location: shell\IContextMenuCB.htm
tech.root: shell
ms.assetid: 1a4c183b-97cf-4c9a-af5a-bcea7c2755a5
ms.date: 12/05/2018
ms.keywords: IContextMenuCB, IContextMenuCB interface [Windows Shell], IContextMenuCB interface [Windows Shell],described, _shell_IContextMenuCB, shell.IContextMenuCB, shobjidl_core/IContextMenuCB
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Shell32.dll (version 6.0.6000 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IContextMenuCB
 - shobjidl_core/IContextMenuCB
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
 - IContextMenuCB
---

# IContextMenuCB interface


## -description

Exposes a method that enables the callback of a context menu. For example, to add a shield icon to a <b>menuItem</b> that requires elevation.

## -inheritance

The <b>IContextMenuCB</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IContextMenuCB</b> also has these types of members:

## -remarks

This is the callback interface specified in the <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-defcontextmenu">DEFCONTEXTMENU</a> structure passed with the function <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu">SHCreateDefaultContextMenu</a>.

This interface enables <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> implementations to manage context menu messages before, after, and during the context menu handling of these messages.
