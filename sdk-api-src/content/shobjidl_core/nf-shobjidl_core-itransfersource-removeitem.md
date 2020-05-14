---
UID: NF:shobjidl_core.ITransferSource.RemoveItem
title: ITransferSource::RemoveItem (shobjidl_core.h)
description: Removes the item without moving the item to the Recycle Bin.
helpviewer_keywords: ["ITransferSource interface [Windows Shell]","RemoveItem method","ITransferSource.RemoveItem","ITransferSource::RemoveItem","RemoveItem","RemoveItem method [Windows Shell]","RemoveItem method [Windows Shell]","ITransferSource interface","_shell_ITransferSource_RemoveItem","shell.ITransferSource_RemoveItem","shobjidl_core/ITransferSource::RemoveItem"]
old-location: shell\ITransferSource_RemoveItem.htm
tech.root: shell
ms.assetid: 53084f0d-cf78-437a-ae04-43fd78cb9839
ms.date: 12/05/2018
ms.keywords: ITransferSource interface [Windows Shell],RemoveItem method, ITransferSource.RemoveItem, ITransferSource::RemoveItem, RemoveItem, RemoveItem method [Windows Shell], RemoveItem method [Windows Shell],ITransferSource interface, _shell_ITransferSource_RemoveItem, shell.ITransferSource_RemoveItem, shobjidl_core/ITransferSource::RemoveItem
f1_keywords:
- shobjidl_core/ITransferSource.RemoveItem
dev_langs:
- c++
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
- ITransferSource.RemoveItem
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITransferSource::RemoveItem


## -description


Removes the item without moving the item to the Recycle Bin.


## -parameters




### -param psiSource [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> to be removed.


### -param flags [in]

Type: <b><a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_transfer_source_flags">TRANSFER_SOURCE_FLAGS</a></b>

Flags that control the file operation. One or more of the <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_transfer_source_flags">TRANSFER_SOURCE_FLAGS</a> constants.


## -returns



Type: <b>HRESULT</b>

Returns one of the following, or an error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>COPYENGINE_S_YES</b></dt>
</dl>
</td>
<td width="60%">
User responded "Yes" to the dialog

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>COPYENGINE_S_USER_RETRY</b></dt>
</dl>
</td>
<td width="60%">
User responded to retry the current action

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>COPYENGINE_S_USER_IGNORED</b></dt>
</dl>
</td>
<td width="60%">
User responded "No" to the dialog.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>COPYENGINE_S_MERGE</b></dt>
</dl>
</td>
<td width="60%">
User responded to merge folders.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>COPYENGINE_S_USER_RETRY_WITH_NEW_NAME</b></dt>
</dl>
</td>
<td width="60%">
User responded to retry the file with new name.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>COPYENGINE_S_DONT_PROCESS_CHILDREN</b></dt>
</dl>
</td>
<td width="60%">
Child items should not be processed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>COPYENGINE_S_PENDING</b></dt>
</dl>
</td>
<td width="60%">
Error has been queued and will display later.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>COPYENGINE_E_USER_CANCELLED</b></dt>
</dl>
</td>
<td width="60%">
User canceled the current action.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>COPYENGINE_E_REQUIRES_ELEVATION</b></dt>
</dl>
</td>
<td width="60%">
Operation requires elevated privileges.

</td>
</tr>
</table>
 



