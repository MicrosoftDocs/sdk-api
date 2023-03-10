---
UID: NN:shobjidl_core.IContextMenu
title: IContextMenu (shobjidl_core.h)
description: Exposes methods that either create or merge a shortcut menu associated with a Shell object.
helpviewer_keywords: ["IContextMenu","IContextMenu interface [Windows Shell]","IContextMenu interface [Windows Shell]","described","_win32_IContextMenu","_win32_icontextmenu_cpp","shell.IContextMenu","shobjidl_core/IContextMenu"]
old-location: shell\IContextMenu.htm
tech.root: shell
ms.assetid: 6ea0b8f9-4a05-4a4b-adc5-d540eb3287ee
ms.date: 12/05/2018
ms.keywords: IContextMenu, IContextMenu interface [Windows Shell], IContextMenu interface [Windows Shell],described, _win32_IContextMenu, _win32_icontextmenu_cpp, shell.IContextMenu, shobjidl_core/IContextMenu
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
 - IContextMenu
 - shobjidl_core/IContextMenu
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
 - IContextMenu
---

# IContextMenu interface

## -description

Exposes methods that either create or merge a shortcut menu associated with a Shell object. Note that there are several better ways to extend Shell menus. For more information, see <a href="/windows/win32/shell/context-menu-handlers">Creating Shortcut Menu Handlers</a>.

## -inheritance

The <b>IContextMenu</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IContextMenu</b> also has these types of members:

## -remarks

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Implement <b>IContextMenu</b> in the following situations.
			

<ul>
<li>
<a href="/windows/desktop/shell/handlers">Shell extension handlers</a> implement this interface to dynamically add items to a Shell object's shortcut menu.</li>
<li>
<a href="/windows/desktop/shell/nse-works">Namespace extensions</a> implement this interface to specify their object's shortcut menus.</li>
</ul>
For a detailed discussion of how to implement <b>IContextMenu</b>, see <a href="/windows/desktop/shell/context-menu-handlers">Creating Context Menu Handlers</a>.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Applications use <b>IContextMenu</b> to retrieve information about the items in an object's shortcut menu and to invoke the associated commands. To retrieve an object's <b>IContextMenu</b> interface, an application must call the object's <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof">IShellFolder::GetUIObjectOf</a> method.

Shell extension handlers that export this interface must also export <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellextinit">IShellExtInit</a>. For details, see <a href="/windows/desktop/shell/handlers">Creating Shell Extension Handlers</a>.

<div class="alert"><b>Note</b>  <b>Windows Vista and later:</b> Prior to Windows Vista this interface was declared in Shlobj.h.</div>
<div> </div>
<div class="alert"><b>Note</b> Windows 11 refines the behavior of the contextual file operations in the right-click context menu of File Explorer and the Share dialog. Please see  <a href="/windows/apps/get-started/make-apps-great-for-windows">Top 11 things you can do to make your app great on Windows 11 </a>
<div></div>
