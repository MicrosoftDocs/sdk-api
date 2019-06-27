---
UID: NN:shobjidl.INameSpaceTreeControlDropHandler
title: INameSpaceTreeControlDropHandler (shobjidl.h)
author: windows-sdk-content
description: Exposes handler methods for drag-and-drop.
old-location: shell\INameSpaceTreeControlDropHandler.htm
tech.root: shell
ms.assetid: 5d2c1783-daeb-488d-93b9-34df2712d849
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: INameSpaceTreeControlDropHandler, INameSpaceTreeControlDropHandler interface [Windows Shell], INameSpaceTreeControlDropHandler interface [Windows Shell],described, _shell_INameSpaceTreeControlDropHandler, shell.INameSpaceTreeControlDropHandler, shobjidl/INameSpaceTreeControlDropHandler
ms.topic: interface
f1_keywords: 
 - "shobjidl/INameSpaceTreeControlDropHandler"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - INameSpaceTreeControlDropHandler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INameSpaceTreeControlDropHandler interface


## -description


Exposes handler methods for drag-and-drop. Used by the namespace tree control to notify the client of any drag-and-drop operation happening within the control. Provides a way for a client to intercept a drop operation and perform its own action, or to return the desired drop effect.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INameSpaceTreeControlDropHandler</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>INameSpaceTreeControlDropHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INameSpaceTreeControlDropHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-inamespacetreecontroldrophandler-ondragenter">OnDragEnter</a>
</td>
<td align="left" width="63%">
Called on drag enter to set drag effect, as specified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-inamespacetreecontroldrophandler-ondragleave">OnDragLeave</a>
</td>
<td align="left" width="63%">
Called on drag leave for a specified item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-inamespacetreecontroldrophandler-ondragover">OnDragOver</a>
</td>
<td align="left" width="63%">
Called on drag over to set drag effect, as specified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-inamespacetreecontroldrophandler-ondragposition">OnDragPosition</a>
</td>
<td align="left" width="63%">
Called when the item is being dragged within the same level (within the same parent folder) in the tree.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-inamespacetreecontroldrophandler-ondrop">OnDrop</a>
</td>
<td align="left" width="63%">
Called on drop to set drop effect, as specified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-inamespacetreecontroldrophandler-ondropposition">OnDropPosition</a>
</td>
<td align="left" width="63%">
Called when the item is being dropped within the same level (within the same parent folder) in the tree.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>



<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-idroptarget">IDropTarget</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrol">INameSpaceTreeControl</a>
 

 

