---
UID: NF:shobjidl_core.ITransferSource.RenameItem
title: ITransferSource::RenameItem (shobjidl_core.h)
description: Changes the name of an item, returning the IShellItem with the new name.
helpviewer_keywords: ["ITransferSource interface [Windows Shell]","RenameItem method","ITransferSource.RenameItem","ITransferSource::RenameItem","RenameItem","RenameItem method [Windows Shell]","RenameItem method [Windows Shell]","ITransferSource interface","_shell_ITransferSource_RenameItem","shell.ITransferSource_RenameItem","shobjidl_core/ITransferSource::RenameItem"]
old-location: shell\ITransferSource_RenameItem.htm
tech.root: shell
ms.assetid: 793eba59-6d21-4c7b-8fdb-bb7658fc410e
ms.date: 12/05/2018
ms.keywords: ITransferSource interface [Windows Shell],RenameItem method, ITransferSource.RenameItem, ITransferSource::RenameItem, RenameItem, RenameItem method [Windows Shell], RenameItem method [Windows Shell],ITransferSource interface, _shell_ITransferSource_RenameItem, shell.ITransferSource_RenameItem, shobjidl_core/ITransferSource::RenameItem
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
 - ITransferSource::RenameItem
 - shobjidl_core/ITransferSource::RenameItem
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
 - ITransferSource.RenameItem
---

# ITransferSource::RenameItem


## -description

Changes the name of an item, returning the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> with the new name.

## -parameters

### -param psiSource [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> object to be renamed.

### -param pszNewName [in]

Type: <b>LPCWSTR</b>

A pointer to a null-terminated, Unicode string containing the new name.

### -param flags [in]

Type: <b><a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_transfer_source_flags">TRANSFER_SOURCE_FLAGS</a></b>

Flags that control the file operation. One or more of the <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_transfer_source_flags">TRANSFER_SOURCE_FLAGS</a> constants.

### -param ppsiNewDest [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>**</b>

When this method returns, contains the address of a pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> object.

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
User responded "Yes" to the dialog.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>COPYENGINE_S_USER_RETRY</b></dt>
</dl>
</td>
<td width="60%">
User responded to retry the current action.

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