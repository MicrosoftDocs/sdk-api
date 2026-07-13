---
UID: NN:shobjidl_core.IContextMenu3
title: IContextMenu3 (shobjidl_core.h)
description: Exposes methods that either create or merge a shortcut menu associated with a Shell object. Allows client objects to handle messages associated with owner-drawn menu items and extends IContextMenu2 by accepting a return value from that message handling.
helpviewer_keywords: ["IContextMenu3","IContextMenu3 interface [Windows Shell]","IContextMenu3 interface [Windows Shell]","described","_win32_IContextMenu3","shell.IContextMenu3","shobjidl_core/IContextMenu3"]
old-location: shell\IContextMenu3.htm
tech.root: shell
ms.assetid: c08e1b98-2b8b-41f6-93c5-3a5937bd3b2c
ms.date: 12/05/2018
ms.keywords: IContextMenu3, IContextMenu3 interface [Windows Shell], IContextMenu3 interface [Windows Shell],described, _win32_IContextMenu3, shell.IContextMenu3, shobjidl_core/IContextMenu3
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IContextMenu3
 - shobjidl_core/IContextMenu3
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
 - IContextMenu3
---

# IContextMenu3 interface


## -description

Exposes methods that either create or merge a shortcut menu associated with a Shell object. Allows client objects to handle messages associated with owner-drawn menu items and extends <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2">IContextMenu2</a> by accepting a return value from that message handling.

## -inheritance

The <b>IContextMenu3</b> interface inherits from <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2">IContextMenu2</a>. <b>IContextMenu3</b> also has these types of members:

## -remarks

This interface also provides the methods of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu">IContextMenu</a> and <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2">IContextMenu2</a> interfaces, from which it inherits.

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Implement <b>IContextMenu3</b> if your shortcut menu extension needs to process the <a href="/windows/desktop/menurc/wm-menuchar">WM_MENUCHAR</a> message.

			    

This message is forwarded to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu3-handlemenumsg2">IContextMenu3::HandleMenuMsg2</a> only if a <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> call for an <b>IContextMenu3</b> interface pointer is successful, which indicates that the object supports this interface.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
You do not call this interface directly. <b>IContextMenu3</b> is used by the operating system only when it has confirmed that your application is aware of this interface.

<div class="alert"><b>Note</b>  <b>Windows Vista and later.</b> Prior to Windows Vista this interface was declared in Shlobj.h.</div>
<div> </div>
