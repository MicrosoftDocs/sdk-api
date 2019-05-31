---
UID: NN:shobjidl_core.INameSpaceTreeControl
title: INameSpaceTreeControl (shobjidl_core.h)
author: windows-sdk-content
description: Exposes methods used to view and manipulate nodes in a tree of Shell items.
old-location: shell\INameSpaceTreeControl.htm
tech.root: shell
ms.assetid: 2072cb3c-e540-4708-bfe8-33fff3a190bd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: INameSpaceTreeControl, INameSpaceTreeControl interface [Windows Shell], INameSpaceTreeControl interface [Windows Shell],described, _shell_INameSpaceTreeControl, shell.INameSpaceTreeControl, shobjidl_core/INameSpaceTreeControl
ms.topic: interface
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - INameSpaceTreeControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INameSpaceTreeControl interface


## -description


Exposes methods used to view and manipulate nodes in a tree of Shell items.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INameSpaceTreeControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>INameSpaceTreeControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INameSpaceTreeControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a280d183-9215-43c2-bba3-63c34ba33285">AppendRoot</a>
</td>
<td align="left" width="63%">
Appends a Shell item to the list of roots in a tree.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a17f7261-20a9-4c08-871c-b0bec6ce784c">CollapseAll</a>
</td>
<td align="left" width="63%">
Collapses all of the items in the given tree.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c0c40137-e19b-448c-a327-454b12a5604a">EnsureItemVisible</a>
</td>
<td align="left" width="63%">
Ensures that the given item is visible.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/16fb3e3a-1686-4bdf-9112-564bb85fb601">GetItemCustomState</a>
</td>
<td align="left" width="63%">
Gets the state of the checkbox associated with a given Shell item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/57e7707c-0fe2-4cde-87d8-2d58e7c06bba">GetItemRect</a>
</td>
<td align="left" width="63%">
Gets the <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that describes the size and position of a given item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/78bee2db-6a28-4fcb-9c43-ab411196ab04">GetItemState</a>
</td>
<td align="left" width="63%">
Gets state information about a Shell item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/71ede595-14b6-4e59-854a-af75c02093f8">GetNextItem</a>
</td>
<td align="left" width="63%">
Retrieves the next item in the tree according to which method is requested.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ca957f8c-ac8e-472e-b762-ddc45e20462d">GetRootItems</a>
</td>
<td align="left" width="63%">
Gets an array of the root items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dfc81922-883a-4749-94be-3630853e38c1">GetSelectedItems</a>
</td>
<td align="left" width="63%">
Gets an array of selected Shell items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2287772d-2c06-4d4b-a11e-727dd5de5326">HitTest</a>
</td>
<td align="left" width="63%">
Retrieves the item that a given point is in, if any.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dfc602bd-6e4e-492d-8bf4-1499319adee7">Initialize</a>
</td>
<td align="left" width="63%">
Initializes an <b>INameSpaceTreeControl</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5d487896-a2ee-4bf3-82d8-90f23a4ff213">InsertRoot</a>
</td>
<td align="left" width="63%">
Inserts a Shell item on a root item in a tree.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9d2eb0c1-c90f-47fb-a322-4267d175df22">RemoveAllRoots</a>
</td>
<td align="left" width="63%">
Removes all roots and their children from a tree.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e27e4eca-60f3-47b7-95cd-c004cda78d77">RemoveRoot</a>
</td>
<td align="left" width="63%">
Removes a root and its children from a tree.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a27fa2a3-3e10-4053-b0b6-222c7b517b5a">SetItemCustomState</a>
</td>
<td align="left" width="63%">
Sets the state of the checkbox associated with the Shell item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f57c5abc-0803-409d-9938-3826f9d8058d">SetItemState</a>
</td>
<td align="left" width="63%">
Sets state information for a Shell item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1b518d58-716b-4ae1-8633-e43117363541">SetTheme</a>
</td>
<td align="left" width="63%">
Sets the desktop theme for the current window only.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d59b9772-7061-4ea5-964a-75deb293b407">TreeAdvise</a>
</td>
<td align="left" width="63%">
Enables a client to register with the control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9a0ba832-503a-48d6-80a7-7f6c51d60215">TreeUnadvise</a>
</td>
<td align="left" width="63%">
Enables a client to unregister with the control.

</td>
</tr>
</table> 


## -remarks



To implement this interface use class ID CLSID_NameSpaceTreeControl.



