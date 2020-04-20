---
UID: NN:shobjidl_core.IContextMenuCB
title: IContextMenuCB (shobjidl_core.h)
description: Exposes a method that enables the callback of a context menu. For example, to add a shield icon to a menuItem that requires elevation.helpviewer_keywords: ["IContextMenuCB","IContextMenuCB interface [Windows Shell]","IContextMenuCB interface [Windows Shell]","described","_shell_IContextMenuCB","shell.IContextMenuCB","shobjidl_core/IContextMenuCB"]
old-location: shell\IContextMenuCB.htm
tech.root: shell
ms.assetid: 1a4c183b-97cf-4c9a-af5a-bcea7c2755a5
ms.date: 12/05/2018
ms.keywords: IContextMenuCB, IContextMenuCB interface [Windows Shell], IContextMenuCB interface [Windows Shell],described, _shell_IContextMenuCB, shell.IContextMenuCB, shobjidl_core/IContextMenuCB
f1_keywords:
- shobjidl_core/IContextMenuCB
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Shell32.dll
api_name:
- IContextMenuCB
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IContextMenuCB interface


## -description


Exposes a method that enables the callback of a context menu. For example, to add a shield icon to a <b>menuItem</b> that requires elevation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IContextMenuCB</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IContextMenuCB</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IContextMenuCB</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenucb-callback">CallBack</a>
</td>
<td align="left" width="63%">
Enables the callback function for a context menu.

</td>
</tr>
</table> 


## -remarks



This is the callback interface specified in the <a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/ns-shlobj_core-defcontextmenu">DEFCONTEXTMENU</a> structure passed with the function <a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu">SHCreateDefaultContextMenu</a>.

This interface enables <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> implementations to manage context menu messages before, after, and during the context menu handling of these messages.



