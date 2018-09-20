---
UID: NN:shobjidl.INameSpaceTreeControlEvents
title: INameSpaceTreeControlEvents
author: windows-sdk-content
description: Exposes methods for handling INameSpaceTreeControl events.
old-location: shell\INameSpaceTreeControlEvents.htm
tech.root: shell
ms.assetid: 496fa657-c27c-4f6c-a137-fb0d393aa284
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: INameSpaceTreeControlEvents, INameSpaceTreeControlEvents interface [Windows Shell], INameSpaceTreeControlEvents interface [Windows Shell],described, _shell_INameSpaceTreeControlEvents, shell.INameSpaceTreeControlEvents, shobjidl/INameSpaceTreeControlEvents
ms.prod: windows
ms.technology: windows-sdk
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
 - INameSpaceTreeControlEvents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INameSpaceTreeControlEvents interface


## -description


Exposes methods for handling <a href="https://msdn.microsoft.com/2072cb3c-e540-4708-bfe8-33fff3a190bd">INameSpaceTreeControl</a> events.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INameSpaceTreeControlEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>INameSpaceTreeControlEvents</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/6d562938-9816-4df9-b5b6-0ed52b1e4835">OnAfterContextMenu</a>
</td>
<td align="left" width="63%">
Called after a context menu is displayed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cdc43044-9d0a-4def-956a-f1031314d4cb">OnAfterExpand</a>
</td>
<td align="left" width="63%">
Called after an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> is expanded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aa243592-1cda-4844-8f3c-e9c62083fabb">OnBeforeContextMenu</a>
</td>
<td align="left" width="63%">
Called before a context menu is displayed; allows client to add additional menu entries.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b3cf5edf-061a-434a-b273-dc33fcdd8448">OnBeforeExpand</a>
</td>
<td align="left" width="63%">
Called before an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> is expanded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6d602c9d-7305-41d3-b757-3e9e125c6cbd">OnBeforeItemDelete</a>
</td>
<td align="left" width="63%">
Called before an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> and all of its children are deleted.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c26296ae-f11c-4fe9-a74c-c97472dbcb1e">OnBeforeStateImageChange</a>
</td>
<td align="left" width="63%">
Called before the state icon of the given <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> is changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cf97e4e9-cd4c-48c0-8230-2152c9767ef2">OnBeginLabelEdit</a>
</td>
<td align="left" width="63%">
Called before the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> goes into edit mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/deeb1cc7-e943-47bd-82f0-089fb3f4c3c6">OnEndLabelEdit</a>
</td>
<td align="left" width="63%">
Called after the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> leaves edit mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/57970b8d-2461-43af-8959-c51f27679407">OnGetToolTip</a>
</td>
<td align="left" width="63%">
Enables you to provide a tooltip.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7737e014-8e46-43da-b017-133bbf12b433">OnItemAdded</a>
</td>
<td align="left" width="63%">
Called after an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> has been added.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a595ffd0-edc6-4726-b7b2-ad1aed9e9701">OnItemClick</a>
</td>
<td align="left" width="63%">
Called when the user clicks a button on the mouse.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/be5894ce-bf4c-4738-9096-da9c9d8688ee">OnItemDeleted</a>
</td>
<td align="left" width="63%">
Called after an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> has been deleted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0154d97b-44db-40bf-a202-e97ba318555f">OnItemStateChanged</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ed0f431a-f3e2-4a95-a16e-6e38568dd91f">OnItemStateChanging</a>
</td>
<td align="left" width="63%">
Called before the state of an item changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b5034847-cba9-4ebe-8578-c933234396e2">OnKeyboardInput</a>
</td>
<td align="left" width="63%">
Called when the user presses a key on the keyboard.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/85d0c2f1-b641-4437-90a4-285cfce62c60">OnPropertyItemCommit</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ecc84586-ec37-4ece-a890-6adfc7a94ad6">OnSelectionChanged</a>
</td>
<td align="left" width="63%">
Called when the selection changes.

</td>
</tr>
</table> 


## -remarks



This interface is implemented by a client of namespace control (CLSID_NameSpaceTreeControl) to be advised of namespace control events so that the client may process these events and if not, allow the namespace control to process them.




## -see-also




<a href="https://msdn.microsoft.com/2072cb3c-e540-4708-bfe8-33fff3a190bd">INameSpaceTreeControl</a>
 

 

