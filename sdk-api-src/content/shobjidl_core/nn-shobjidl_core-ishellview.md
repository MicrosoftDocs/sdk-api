---
UID: NN:shobjidl_core.IShellView
title: IShellView (shobjidl_core.h)
author: windows-sdk-content
description: Exposes methods that present a view in the Windows Explorer or folder windows.
old-location: shell\IShellView.htm
tech.root: shell
ms.assetid: 91438583-e4f1-456f-a130-2a45846fd725
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IShellView, IShellView interface [Windows Shell], IShellView interface [Windows Shell],described, _win32_IShellView, _win32_IShellView_cpp, shell.IShellView, shobjidl_core/IShellView
ms.topic: interface
f1_keywords: 
 - "shobjidl_core/IShellView"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellView
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IShellView interface


## -description


Exposes methods that present a view in the Windows Explorer or folder windows.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellView</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-iolewindow">IOleWindow</a>. <b>IShellView</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IShellView</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-addpropertysheetpages">AddPropertySheetPages</a>
</td>
<td align="left" width="63%">
Allows the view to add pages to the <b>Options</b> property sheet from the <b>View</b> menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-createviewwindow">CreateViewWindow</a>
</td>
<td align="left" width="63%">
Creates a view window. This can be either the right pane of Windows Explorer or the client window of a folder window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-destroyviewwindow">DestroyViewWindow</a>
</td>
<td align="left" width="63%">
Destroys the view window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-enablemodeless">EnableModeless</a>
</td>
<td align="left" width="63%">
Enables or disables modeless dialog boxes. This method is not currently implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/bb774830(v=vs.85)">EnableModelessSV</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-getcurrentinfo">GetCurrentInfo</a>
</td>
<td align="left" width="63%">
Gets the current folder settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-getitemobject">GetItemObject</a>
</td>
<td align="left" width="63%">
Gets an interface that refers to data presented in the view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-refresh">Refresh</a>
</td>
<td align="left" width="63%">
Refreshes the view's contents in response to user input.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-saveviewstate">SaveViewState</a>
</td>
<td align="left" width="63%">
Saves the Shell's view settings so the current state can be restored during a subsequent browsing session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-selectitem">SelectItem</a>
</td>
<td align="left" width="63%">
Changes the selection state of one or more items within the Shell view window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-translateaccelerator">TranslateAccelerator</a>
</td>
<td align="left" width="63%">
Translates keyboard shortcut (accelerator) key strokes when a namespace extension's view has the focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-uiactivate">UIActivate</a>
</td>
<td align="left" width="63%">
Called when the activation state of the view window is changed by an event that is not caused by the Shell view itself. For example, if the TAB key is pressed when the tree has the focus, the view should be given the focus.

</td>
</tr>
</table> 


## -remarks



The object that exposes <b>IShellView</b> is typically created by a call to the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-createviewobject">IShellFolder::CreateViewObject</a> method. This provides the channel of communication between a view object and Windows Explorer's outermost frame window. The communication involves the translation of messages, the state of the frame window (activated or deactivated), the state of the document window (activated or deactivated), and the merging of menus and toolbar items.

This interface is implemented by namespace extensions that display themselves in Windows Explorer's namespace. This object is created by the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> object that hosts the view.

These methods are used by the Shell view's Windows Explorer window to manipulate objects while they are active.

<b>IShellView</b> is derived from <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-iolewindow">IOleWindow</a>. The listed methods are specific to <b>IShellView</b>.

A special instance of <b>IShellView</b> known as the default Shell folder view object can be created by calling <a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview">SHCreateShellFolderView</a> or <a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex">SHCreateShellFolderViewEx</a>. This instance can be differentiated from standard implementations by calling <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> on an <b>IShellView</b> object using the IID_CDefView IID. This call succeeds only when made on the default Shell folder view object.



