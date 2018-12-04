---
UID: NN:shobjidl.INameSpaceTreeControlDropHandler
title: INameSpaceTreeControlDropHandler
author: windows-sdk-content
description: Exposes handler methods for drag-and-drop.
old-location: shell\INameSpaceTreeControlDropHandler.htm
tech.root: shell
ms.assetid: 5d2c1783-daeb-488d-93b9-34df2712d849
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: INameSpaceTreeControlDropHandler, INameSpaceTreeControlDropHandler interface [Windows Shell], INameSpaceTreeControlDropHandler interface [Windows Shell],described, _shell_INameSpaceTreeControlDropHandler, shell.INameSpaceTreeControlDropHandler, shobjidl/INameSpaceTreeControlDropHandler
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
---

# INameSpaceTreeControlDropHandler interface


## -description


Exposes handler methods for drag-and-drop. Used by the namespace tree control to notify the client of any drag-and-drop operation happening within the control. Provides a way for a client to intercept a drop operation and perform its own action, or to return the desired drop effect.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INameSpaceTreeControlDropHandler</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>INameSpaceTreeControlDropHandler</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/b9a87024-d62e-4006-a716-c1461d9c9ffe">OnDragEnter</a>
</td>
<td align="left" width="63%">
Called on drag enter to set drag effect, as specified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b5c67541-dcc2-412f-84aa-df0b0d135597">OnDragLeave</a>
</td>
<td align="left" width="63%">
Called on drag leave for a specified item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9875bd38-9f1d-479f-bd8a-8deb07aa9b53">OnDragOver</a>
</td>
<td align="left" width="63%">
Called on drag over to set drag effect, as specified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b3f49da1-81a0-4d54-a2c3-5cb76f8a02de">OnDragPosition</a>
</td>
<td align="left" width="63%">
Called when the item is being dragged within the same level (within the same parent folder) in the tree.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/05c677fb-a2e2-4aa5-bb27-4dc437ca408c">OnDrop</a>
</td>
<td align="left" width="63%">
Called on drop to set drop effect, as specified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/72d14961-85d1-428c-b2de-70c49c91b5b0">OnDropPosition</a>
</td>
<td align="left" width="63%">
Called when the item is being dropped within the same level (within the same parent folder) in the tree.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>



<a href="https://msdn.microsoft.com/13fbe834-1ef8-4944-b2e4-9f5c413c65c8">IDropTarget</a>



<a href="https://msdn.microsoft.com/2072cb3c-e540-4708-bfe8-33fff3a190bd">INameSpaceTreeControl</a>
 

 

