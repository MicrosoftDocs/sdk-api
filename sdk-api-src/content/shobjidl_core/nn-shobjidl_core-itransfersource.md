---
UID: NN:shobjidl_core.ITransferSource
title: ITransferSource (shobjidl_core.h)
description: Exposes methods to manipulate IShellItem, including copy, move, recycle, and others. This interface is offered to provide more control over file operations by providing an ITransferSource::Advise method.
helpviewer_keywords: ["ITransferSource","ITransferSource interface [Windows Shell]","ITransferSource interface [Windows Shell]","described","_shell_ITransferSource","shell.ITransferSource","shobjidl_core/ITransferSource"]
old-location: shell\ITransferSource.htm
tech.root: shell
ms.assetid: 341966d4-f9cf-457d-97ef-8e6107544283
ms.date: 12/05/2018
ms.keywords: ITransferSource, ITransferSource interface [Windows Shell], ITransferSource interface [Windows Shell],described, _shell_ITransferSource, shell.ITransferSource, shobjidl_core/ITransferSource
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
 - ITransferSource
 - shobjidl_core/ITransferSource
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
 - ITransferSource
---

# ITransferSource interface


## -description

 Exposes methods to manipulate <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>, including copy, move, recycle, and others. This interface is offered to provide more control over file operations by providing an <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransfersource-advise">ITransferSource::Advise</a> method.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITransferSource</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITransferSource</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransfersource-advise">Advise</a>
</td>
<td align="left" width="63%">
Sets up an advisory connection for notifications on the status of file operations.
       

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransfersource-applypropertiestoitem">ApplyPropertiesToItem</a>
</td>
<td align="left" width="63%">
Apply a set of property changes to an item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransfersource-enterfolder">EnterFolder</a>
</td>
<td align="left" width="63%">
Notifies that a folder is the destination of a file operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransfersource-getdefaultdestinationname">GetDefaultDestinationName</a>
</td>
<td align="left" width="63%">
Gets the default name for a Shell item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransfersource-leavefolder">LeaveFolder</a>
</td>
<td align="left" width="63%">
Sends notification that a folder is no longer the destination of a file operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransfersource-linkitem">LinkItem</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransfersource-moveitem">MoveItem</a>
</td>
<td align="left" width="63%">
Moves the item within the volume/namespace, returning the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> in its new location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransfersource-openitem">OpenItem</a>
</td>
<td align="left" width="63%">
Opens the item for copying. Returns an object that can be enumerated for resources (<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemresources">IShellItemResources</a>).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransfersource-recycleitem">RecycleItem</a>
</td>
<td align="left" width="63%">
Recycle the item into the provided recycle location and return the item in its new location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransfersource-removeitem">RemoveItem</a>
</td>
<td align="left" width="63%">
Removes the item without moving the item to the Recycle Bin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransfersource-renameitem">RenameItem</a>
</td>
<td align="left" width="63%">
Changes the name of an item, returning the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> with the new name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransfersource-setproperties">SetProperties</a>
</td>
<td align="left" width="63%">
Sets properties that should be applied to an item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransfersource-unadvise">Unadvise</a>
</td>
<td align="left" width="63%">
Terminates an advisory connection.

</td>
</tr>
</table>

