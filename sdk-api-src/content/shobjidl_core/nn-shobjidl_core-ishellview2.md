---
UID: NN:shobjidl_core.IShellView2
title: IShellView2 (shobjidl_core.h)
description: Extends the capabilities of IShellView.helpviewer_keywords: ["IShellView2","IShellView2 interface [Windows Shell]","IShellView2 interface [Windows Shell]","described","_win32_IShellView2","shell.IShellView2","shobjidl_core/IShellView2"]
old-location: shell\IShellView2.htm
tech.root: shell
ms.assetid: a61aec39-406d-4066-941d-e788d64f4310
ms.date: 12/05/2018
ms.keywords: IShellView2, IShellView2 interface [Windows Shell], IShellView2 interface [Windows Shell],described, _win32_IShellView2, shell.IShellView2, shobjidl_core/IShellView2
f1_keywords:
- shobjidl_core/IShellView2
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Shell32.dll
api_name:
- IShellView2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IShellView2 interface


## -description


Extends the capabilities of <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellView2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a>. <b>IShellView2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IShellView2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview2-createviewwindow2">CreateViewWindow2</a>
</td>
<td align="left" width="63%">
Used to request the creation of a new Shell view window. It can be either the right pane of Windows Explorer or the client window of a folder window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview2-getview">GetView</a>
</td>
<td align="left" width="63%">
Requests the current or default Shell view, together with all other valid view identifiers (VIDs) supported by this implementation of <b>IShellView2</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview2-handlerename">HandleRename</a>
</td>
<td align="left" width="63%">
Used to change an item's identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview2-selectandpositionitem">SelectAndPositionItem</a>
</td>
<td align="left" width="63%">
Selects and positions an item in a Shell View.

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a> interface, from which it inherits.

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Implement <b>IShellView2</b> if your namespace extension provides services to clients beyond those in <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a>.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
You do not call this interface directly. <b>IShellView2</b> is used by the operating system only when it has confirmed that your application is aware of this interface. Objects that expose <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a> and <b>IShellView2</b> are usually created by other Shell folder objects.



