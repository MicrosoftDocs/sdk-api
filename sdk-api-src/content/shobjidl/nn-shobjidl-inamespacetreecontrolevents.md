---
UID: NN:shobjidl.INameSpaceTreeControlEvents
title: INameSpaceTreeControlEvents (shobjidl.h)
description: Exposes methods for handling INameSpaceTreeControl events.
helpviewer_keywords: ["INameSpaceTreeControlEvents","INameSpaceTreeControlEvents interface [Windows Shell]","INameSpaceTreeControlEvents interface [Windows Shell]","described","_shell_INameSpaceTreeControlEvents","shell.INameSpaceTreeControlEvents","shobjidl/INameSpaceTreeControlEvents"]
old-location: shell\INameSpaceTreeControlEvents.htm
tech.root: shell
ms.assetid: 496fa657-c27c-4f6c-a137-fb0d393aa284
ms.date: 12/05/2018
ms.keywords: INameSpaceTreeControlEvents, INameSpaceTreeControlEvents interface [Windows Shell], INameSpaceTreeControlEvents interface [Windows Shell],described, _shell_INameSpaceTreeControlEvents, shell.INameSpaceTreeControlEvents, shobjidl/INameSpaceTreeControlEvents
req.header: shobjidl.h
req.include-header: 
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
 - INameSpaceTreeControlEvents
 - shobjidl/INameSpaceTreeControlEvents
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - INameSpaceTreeControlEvents
---

# INameSpaceTreeControlEvents interface


## -description

Exposes methods for handling <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrol">INameSpaceTreeControl</a> events.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INameSpaceTreeControlEvents</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>INameSpaceTreeControlEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INameSpaceTreeControlEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-inamespacetreecontrolevents-onaftercontextmenu">OnAfterContextMenu</a>
</td>
<td align="left" width="63%">
Called after a context menu is displayed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-inamespacetreecontrolevents-onafterexpand">OnAfterExpand</a>
</td>
<td align="left" width="63%">
Called after an <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> is expanded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-inamespacetreecontrolevents-onbeforecontextmenu">OnBeforeContextMenu</a>
</td>
<td align="left" width="63%">
Called before a context menu is displayed; allows client to add additional menu entries.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-inamespacetreecontrolevents-onbeforeexpand">OnBeforeExpand</a>
</td>
<td align="left" width="63%">
Called before an <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> is expanded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-inamespacetreecontrolevents-onbeforeitemdelete">OnBeforeItemDelete</a>
</td>
<td align="left" width="63%">
Called before an <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> and all of its children are deleted.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-inamespacetreecontrolevents-onbeforestateimagechange">OnBeforeStateImageChange</a>
</td>
<td align="left" width="63%">
Called before the state icon of the given <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> is changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-inamespacetreecontrolevents-onbeginlabeledit">OnBeginLabelEdit</a>
</td>
<td align="left" width="63%">
Called before the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> goes into edit mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-inamespacetreecontrolevents-onendlabeledit">OnEndLabelEdit</a>
</td>
<td align="left" width="63%">
Called after the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> leaves edit mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-inamespacetreecontrolevents-ongettooltip">OnGetToolTip</a>
</td>
<td align="left" width="63%">
Enables you to provide a tooltip.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-inamespacetreecontrolevents-onitemadded">OnItemAdded</a>
</td>
<td align="left" width="63%">
Called after an <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> has been added.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-inamespacetreecontrolevents-onitemclick">OnItemClick</a>
</td>
<td align="left" width="63%">
Called when the user clicks a button on the mouse.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-inamespacetreecontrolevents-onitemdeleted">OnItemDeleted</a>
</td>
<td align="left" width="63%">
Called after an <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> has been deleted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-inamespacetreecontrolevents-onitemstatechanged">OnItemStateChanged</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-inamespacetreecontrolevents-onitemstatechanging">OnItemStateChanging</a>
</td>
<td align="left" width="63%">
Called before the state of an item changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-inamespacetreecontrolevents-onkeyboardinput">OnKeyboardInput</a>
</td>
<td align="left" width="63%">
Called when the user presses a key on the keyboard.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-inamespacetreecontrolevents-onpropertyitemcommit">OnPropertyItemCommit</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-inamespacetreecontrolevents-onselectionchanged">OnSelectionChanged</a>
</td>
<td align="left" width="63%">
Called when the selection changes.

</td>
</tr>
</table>

## -remarks

This interface is implemented by a client of namespace control (CLSID_NameSpaceTreeControl) to be advised of namespace control events so that the client may process these events and if not, allow the namespace control to process them.

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrol">INameSpaceTreeControl</a>

