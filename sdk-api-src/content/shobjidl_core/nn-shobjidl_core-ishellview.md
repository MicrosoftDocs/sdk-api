---
UID: NN:shobjidl_core.IShellView
title: IShellView (shobjidl_core.h)
description: Exposes methods that present a view in the Windows Explorer or folder windows.
helpviewer_keywords: ["IShellView","IShellView interface [Windows Shell]","IShellView interface [Windows Shell]","described","_win32_IShellView","_win32_IShellView_cpp","shell.IShellView","shobjidl_core/IShellView"]
old-location: shell\IShellView.htm
tech.root: shell
ms.assetid: 91438583-e4f1-456f-a130-2a45846fd725
ms.date: 12/05/2018
ms.keywords: IShellView, IShellView interface [Windows Shell], IShellView interface [Windows Shell],described, _win32_IShellView, _win32_IShellView_cpp, shell.IShellView, shobjidl_core/IShellView
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellView
 - shobjidl_core/IShellView
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
 - IShellView
---

# IShellView interface


## -description

Exposes methods that present a view in the Windows Explorer or folder windows.

## -inheritance

The <b>IShellView</b> interface inherits from <a href="/windows/desktop/api/oleidl/nn-oleidl-iolewindow">IOleWindow</a>. <b>IShellView</b> also has these types of members:

## -remarks

The object that exposes <b>IShellView</b> is typically created by a call to the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-createviewobject">IShellFolder::CreateViewObject</a> method. This provides the channel of communication between a view object and Windows Explorer's outermost frame window. The communication involves the translation of messages, the state of the frame window (activated or deactivated), the state of the document window (activated or deactivated), and the merging of menus and toolbar items.

This interface is implemented by namespace extensions that display themselves in Windows Explorer's namespace. This object is created by the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> object that hosts the view.

These methods are used by the Shell view's Windows Explorer window to manipulate objects while they are active.

<b>IShellView</b> is derived from <a href="/windows/desktop/api/oleidl/nn-oleidl-iolewindow">IOleWindow</a>. The listed methods are specific to <b>IShellView</b>.

A special instance of <b>IShellView</b> known as the default Shell folder view object can be created by calling <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview">SHCreateShellFolderView</a> or <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex">SHCreateShellFolderViewEx</a>. This instance can be differentiated from standard implementations by calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on an <b>IShellView</b> object using the IID_CDefView IID. This call succeeds only when made on the default Shell folder view object.
