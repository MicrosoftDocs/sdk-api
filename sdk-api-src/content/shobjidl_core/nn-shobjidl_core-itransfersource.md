---
UID: NN:shobjidl_core.ITransferSource
title: ITransferSource
author: windows-sdk-content
description: Exposes methods to manipulate IShellItem, including copy, move, recycle, and others. This interface is offered to provide more control over file operations by providing an ITransferSource::Advise method.
old-location: shell\ITransferSource.htm
tech.root: shell
ms.assetid: 341966d4-f9cf-457d-97ef-8e6107544283
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: ITransferSource, ITransferSource interface [Windows Shell], ITransferSource interface [Windows Shell],described, _shell_ITransferSource, shell.ITransferSource, shobjidl_core/ITransferSource
ms.prod: windows
ms.technology: windows-sdk
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
 - ITransferSource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITransferSource interface


## -description


 Exposes methods to manipulate <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>, including copy, move, recycle, and others. This interface is offered to provide more control over file operations by providing an <a href="https://msdn.microsoft.com/5a546603-d409-4c8e-9fa8-892c5c4844e7">ITransferSource::Advise</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITransferSource</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITransferSource</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITransferSource</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5a546603-d409-4c8e-9fa8-892c5c4844e7">Advise</a>
</td>
<td align="left" width="63%">
Sets up an advisory connection for notifications on the status of file operations.
       

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f3a99637-8ce7-4177-bcf7-716ed7698934">ApplyPropertiesToItem</a>
</td>
<td align="left" width="63%">
Apply a set of property changes to an item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/de6b1b03-450f-4d48-b0f4-67e268feb36a">EnterFolder</a>
</td>
<td align="left" width="63%">
Notifies that a folder is the destination of a file operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a99d9622-b205-4a8a-9840-879f655463a5">GetDefaultDestinationName</a>
</td>
<td align="left" width="63%">
Gets the default name for a Shell item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c8d0b757-a103-4c18-b556-8ba4ea9b3a2d">LeaveFolder</a>
</td>
<td align="left" width="63%">
Sends notification that a folder is no longer the destination of a file operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e373c790-5366-4bff-a08d-817b0c566b1d">LinkItem</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/de59291c-12ad-4639-bc10-d8416a979eb7">MoveItem</a>
</td>
<td align="left" width="63%">
Moves the item within the volume/namespace, returning the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> in its new location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8f051923-2798-43e9-8e8d-95eec5f618aa">OpenItem</a>
</td>
<td align="left" width="63%">
Opens the item for copying. Returns an object that can be enumerated for resources (<a href="https://msdn.microsoft.com/4ca4a01e-e3c2-46aa-a700-b4b2a1e0112e">IShellItemResources</a>).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ee99a1ff-1a3e-46a4-82c6-df5f6c26c396">RecycleItem</a>
</td>
<td align="left" width="63%">
Recycle the item into the provided recycle location and return the item in its new location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/53084f0d-cf78-437a-ae04-43fd78cb9839">RemoveItem</a>
</td>
<td align="left" width="63%">
Removes the item without moving the item to the Recycle Bin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/793eba59-6d21-4c7b-8fdb-bb7658fc410e">RenameItem</a>
</td>
<td align="left" width="63%">
Changes the name of an item, returning the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> with the new name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c42497cc-5a19-41da-9356-1086796032a7">SetProperties</a>
</td>
<td align="left" width="63%">
Sets properties that should be applied to an item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4f71134e-dfbf-40e7-b72b-c4913c876689">Unadvise</a>
</td>
<td align="left" width="63%">
Terminates an advisory connection.

</td>
</tr>
</table> 

