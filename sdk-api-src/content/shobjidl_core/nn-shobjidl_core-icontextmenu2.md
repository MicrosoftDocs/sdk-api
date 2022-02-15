---
UID: NN:shobjidl_core.IContextMenu2
title: IContextMenu2 (shobjidl_core.h)
description: Exposes methods that either create or merge a shortcut (context) menu associated with a Shell object. Extends IContextMenu by adding a method that allows client objects to handle messages associated with owner-drawn menu items.
helpviewer_keywords: ["IContextMenu2","IContextMenu2 interface [Windows Shell]","IContextMenu2 interface [Windows Shell]","described","_win32_IContextMenu2","shell.IContextMenu2","shobjidl_core/IContextMenu2"]
old-location: shell\IContextMenu2.htm
tech.root: shell
ms.assetid: 4e3331ad-4adc-4ea9-8a22-6aad15f618c8
ms.date: 12/05/2018
ms.keywords: IContextMenu2, IContextMenu2 interface [Windows Shell], IContextMenu2 interface [Windows Shell],described, _win32_IContextMenu2, shell.IContextMenu2, shobjidl_core/IContextMenu2
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
 - IContextMenu2
 - shobjidl_core/IContextMenu2
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
 - IContextMenu2
---

# IContextMenu2 interface


## -description

Exposes methods that either create or merge a shortcut (context) menu associated with a Shell object. Extends <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu">IContextMenu</a> by adding a method that allows client objects to handle messages associated with owner-drawn menu items.

## -inheritance

The <b>IContextMenu2</b> interface inherits from <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu">IContextMenu</a>. <b>IContextMenu2</b> also has these types of members:

## -remarks

This interface also provides the methods of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu">IContextMenu</a> interface, from which it inherits.

<div class="alert"><b>Note</b>  <b>Windows Vista and later.</b> Prior to Windows Vista this interface was declared in Shlobj.h.</div>
<div> </div>
<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Implement <b>IContextMenu2</b> if your <a href="/windows/desktop/shell/nse-works">namespace extension</a> or <a href="/windows/desktop/shell/context-menu-handlers">shortcut menu handler</a> needs to process one or more of the following messages. 

				

<ul>
<li>
<a href="/windows/desktop/menurc/wm-initmenupopup">WM_INITMENUPOPUP</a>
</li>
<li>
<a href="/windows/desktop/Controls/wm-drawitem">WM_DRAWITEM</a>
</li>
<li>
<a href="/windows/desktop/Controls/wm-measureitem">WM_MEASUREITEM</a>
</li>
</ul>
These messages are forwarded to <b>IContextMenu2</b>—through the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu2-handlemenumsg">HandleMenuMsg</a> method—only if a <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> call for an <b>IContextMenu2</b> interface pointer is successful, indicating that the object supports this interface.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Applications do not normally call this interface directly.
