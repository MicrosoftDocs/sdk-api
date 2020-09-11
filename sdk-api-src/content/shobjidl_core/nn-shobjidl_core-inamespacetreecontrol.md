---
UID: NN:shobjidl_core.INameSpaceTreeControl
title: INameSpaceTreeControl (shobjidl_core.h)
description: Exposes methods used to view and manipulate nodes in a tree of Shell items.
helpviewer_keywords: ["INameSpaceTreeControl","INameSpaceTreeControl interface [Windows Shell]","INameSpaceTreeControl interface [Windows Shell]","described","_shell_INameSpaceTreeControl","shell.INameSpaceTreeControl","shobjidl_core/INameSpaceTreeControl"]
old-location: shell\INameSpaceTreeControl.htm
tech.root: shell
ms.assetid: 2072cb3c-e540-4708-bfe8-33fff3a190bd
ms.date: 12/05/2018
ms.keywords: INameSpaceTreeControl, INameSpaceTreeControl interface [Windows Shell], INameSpaceTreeControl interface [Windows Shell],described, _shell_INameSpaceTreeControl, shell.INameSpaceTreeControl, shobjidl_core/INameSpaceTreeControl
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INameSpaceTreeControl
 - shobjidl_core/INameSpaceTreeControl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - INameSpaceTreeControl
---

# INameSpaceTreeControl interface


## -description

Exposes methods used to view and manipulate nodes in a tree of Shell items.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INameSpaceTreeControl</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>INameSpaceTreeControl</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-inamespacetreecontrol-appendroot">AppendRoot</a>
</td>
<td align="left" width="63%">
Appends a Shell item to the list of roots in a tree.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-inamespacetreecontrol-collapseall">CollapseAll</a>
</td>
<td align="left" width="63%">
Collapses all of the items in the given tree.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-inamespacetreecontrol-ensureitemvisible">EnsureItemVisible</a>
</td>
<td align="left" width="63%">
Ensures that the given item is visible.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-inamespacetreecontrol-getitemcustomstate">GetItemCustomState</a>
</td>
<td align="left" width="63%">
Gets the state of the checkbox associated with a given Shell item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-inamespacetreecontrol-getitemrect">GetItemRect</a>
</td>
<td align="left" width="63%">
Gets the <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that describes the size and position of a given item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-inamespacetreecontrol-getitemstate">GetItemState</a>
</td>
<td align="left" width="63%">
Gets state information about a Shell item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-inamespacetreecontrol-getnextitem">GetNextItem</a>
</td>
<td align="left" width="63%">
Retrieves the next item in the tree according to which method is requested.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-inamespacetreecontrol-getrootitems">GetRootItems</a>
</td>
<td align="left" width="63%">
Gets an array of the root items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-inamespacetreecontrol-getselecteditems">GetSelectedItems</a>
</td>
<td align="left" width="63%">
Gets an array of selected Shell items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-inamespacetreecontrol-hittest">HitTest</a>
</td>
<td align="left" width="63%">
Retrieves the item that a given point is in, if any.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-inamespacetreecontrol-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes an <b>INameSpaceTreeControl</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-inamespacetreecontrol-insertroot">InsertRoot</a>
</td>
<td align="left" width="63%">
Inserts a Shell item on a root item in a tree.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-inamespacetreecontrol-removeallroots">RemoveAllRoots</a>
</td>
<td align="left" width="63%">
Removes all roots and their children from a tree.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-inamespacetreecontrol-removeroot">RemoveRoot</a>
</td>
<td align="left" width="63%">
Removes a root and its children from a tree.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-inamespacetreecontrol-setitemcustomstate">SetItemCustomState</a>
</td>
<td align="left" width="63%">
Sets the state of the checkbox associated with the Shell item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-inamespacetreecontrol-setitemstate">SetItemState</a>
</td>
<td align="left" width="63%">
Sets state information for a Shell item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-inamespacetreecontrol-settheme">SetTheme</a>
</td>
<td align="left" width="63%">
Sets the desktop theme for the current window only.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-inamespacetreecontrol-treeadvise">TreeAdvise</a>
</td>
<td align="left" width="63%">
Enables a client to register with the control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-inamespacetreecontrol-treeunadvise">TreeUnadvise</a>
</td>
<td align="left" width="63%">
Enables a client to unregister with the control.

</td>
</tr>
</table>

## -remarks

To implement this interface use class ID CLSID_NameSpaceTreeControl.

