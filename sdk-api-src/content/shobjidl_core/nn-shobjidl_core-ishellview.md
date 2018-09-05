---
UID: NN:shobjidl_core.IShellView
title: IShellView
author: windows-sdk-content
description: Exposes methods that present a view in the Windows Explorer or folder windows.
old-location: shell\IShellView.htm
old-project: shell
ms.assetid: 91438583-e4f1-456f-a130-2a45846fd725
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IShellView, IShellView interface [Windows Shell], IShellView interface [Windows Shell],described, _win32_IShellView, _win32_IShellView_cpp, shell.IShellView, shobjidl_core/IShellView
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellView
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IShellView interface


## -description


Exposes methods that present a view in the Windows Explorer or folder windows.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellView</b> interface inherits from <a href="https://msdn.microsoft.com/2d0efbae-4a1c-43b1-9021-8d89377f7282">IOleWindow</a>. <b>IShellView</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/6f05ddf7-190e-41f5-b24a-d18112b34600">AddPropertySheetPages</a>
</td>
<td align="left" width="63%">
Allows the view to add pages to the <b>Options</b> property sheet from the <b>View</b> menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/62d71bca-d2cb-4668-b0bf-2e53756f2cd9">CreateViewWindow</a>
</td>
<td align="left" width="63%">
Creates a view window. This can be either the right pane of Windows Explorer or the client window of a folder window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b0dfc200-4438-4f11-a426-c82eeb9cc745">DestroyViewWindow</a>
</td>
<td align="left" width="63%">
Destroys the view window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5467f524-fa61-4919-bf64-268f9387b2f2">EnableModeless</a>
</td>
<td align="left" width="63%">
Enables or disables modeless dialog boxes. This method is not currently implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8d90cbe0-1795-4c13-9087-6b4268fefdd4">EnableModelessSV</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/69d18b4f-3a68-420c-a184-05c2f69a5ec6">GetCurrentInfo</a>
</td>
<td align="left" width="63%">
Gets the current folder settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/249ce8cc-6820-4f0a-a83a-2035e88d0d9c">GetItemObject</a>
</td>
<td align="left" width="63%">
Gets an interface that refers to data presented in the view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/510aea71-5885-4d23-8fe9-1fef4881cb18">Refresh</a>
</td>
<td align="left" width="63%">
Refreshes the view's contents in response to user input.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4bc36340-1e52-48cf-8b9a-e32115cda88b">SaveViewState</a>
</td>
<td align="left" width="63%">
Saves the Shell's view settings so the current state can be restored during a subsequent browsing session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5c34c05e-175c-43cb-9fbb-2eb3e2b39f6f">SelectItem</a>
</td>
<td align="left" width="63%">
Changes the selection state of one or more items within the Shell view window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/425a281e-2d34-4bb3-92b9-05ae4cf70a9f">TranslateAccelerator</a>
</td>
<td align="left" width="63%">
Translates keyboard shortcut (accelerator) key strokes when a namespace extension's view has the focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/169881de-d073-4864-beb2-4e030b855e8f">UIActivate</a>
</td>
<td align="left" width="63%">
Called when the activation state of the view window is changed by an event that is not caused by the Shell view itself. For example, if the TAB key is pressed when the tree has the focus, the view should be given the focus.

</td>
</tr>
</table> 


## -remarks



The object that exposes <b>IShellView</b> is typically created by a call to the <a href="https://msdn.microsoft.com/8a1b73ad-6719-403a-a8aa-27bef537b7a9">IShellFolder::CreateViewObject</a> method. This provides the channel of communication between a view object and Windows Explorer's outermost frame window. The communication involves the translation of messages, the state of the frame window (activated or deactivated), the state of the document window (activated or deactivated), and the merging of menus and toolbar items.

This interface is implemented by namespace extensions that display themselves in Windows Explorer's namespace. This object is created by the <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a> object that hosts the view.

These methods are used by the Shell view's Windows Explorer window to manipulate objects while they are active.

<b>IShellView</b> is derived from <a href="https://msdn.microsoft.com/2d0efbae-4a1c-43b1-9021-8d89377f7282">IOleWindow</a>. The listed methods are specific to <b>IShellView</b>.

A special instance of <b>IShellView</b> known as the default Shell folder view object can be created by calling <a href="https://msdn.microsoft.com/f2948a6d-84a5-456b-b328-ba76dba46e9d">SHCreateShellFolderView</a> or <a href="https://msdn.microsoft.com/7edd6786-7d74-4065-8cf1-cbb489007a46">SHCreateShellFolderViewEx</a>. This instance can be differentiated from standard implementations by calling <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> on an <b>IShellView</b> object using the IID_CDefView IID. This call succeeds only when made on the default Shell folder view object.



