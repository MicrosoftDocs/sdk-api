---
UID: NF:shobjidl_core.ITransferSource.MoveItem
title: ITransferSource::MoveItem (shobjidl_core.h)
description: Moves the item within the volume/namespace, returning the IShellItem in its new location.
helpviewer_keywords: ["ITransferSource interface [Windows Shell]","MoveItem method","ITransferSource.MoveItem","ITransferSource::MoveItem","MoveItem","MoveItem method [Windows Shell]","MoveItem method [Windows Shell]","ITransferSource interface","_shell_ITransferSource_MoveItem","shell.ITransferSource_MoveItem","shobjidl_core/ITransferSource::MoveItem"]
old-location: shell\ITransferSource_MoveItem.htm
tech.root: shell
ms.assetid: de59291c-12ad-4639-bc10-d8416a979eb7
ms.date: 12/05/2018
ms.keywords: ITransferSource interface [Windows Shell],MoveItem method, ITransferSource.MoveItem, ITransferSource::MoveItem, MoveItem, MoveItem method [Windows Shell], MoveItem method [Windows Shell],ITransferSource interface, _shell_ITransferSource_MoveItem, shell.ITransferSource_MoveItem, shobjidl_core/ITransferSource::MoveItem
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
 - ITransferSource::MoveItem
 - shobjidl_core/ITransferSource::MoveItem
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
 - ITransferSource.MoveItem
---

# ITransferSource::MoveItem


## -description

Moves the item within the volume/namespace, returning the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> in its new location.

## -parameters

### -param psi [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> to be moved.

### -param psiParentDst [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> that represents the new parent item at the destination.

### -param pszNameDst [in]

Type: <b>LPCWSTR</b>

Pointer to a null-terminated buffer that contains the destination path.

### -param flags

Type: <b><a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_transfer_source_flags">TRANSFER_SOURCE_FLAGS</a></b>

Flags that control the file operation. One or more of the <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_transfer_source_flags">TRANSFER_SOURCE_FLAGS</a> constants.

### -param ppsiNew [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>**</b>

When this method returns successfully, contains an address of a pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> in its new location.

## -returns

Type: <b>HRESULT</b>

Returns <b>S_OK</b> if the move succeeded. In that case, <i>ppsiNew</i> points to the address of the new item. Other possible return values, both success and failure codes, include the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>COPYENGINE_S_USER_IGNORED</b></dt>
</dl>
</td>
<td width="60%">
The destination item already exists and has not been overwritten. In this case, <i>ppsiNew</i> is <b>NULL</b> and the caller should delete the source item.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>COPYENGINE_S_MERGE</b></dt>
</dl>
</td>
<td width="60%">
The destination item already exists and the user has chosen to merge the source and destination folders. In this case, <i>ppsiNew</i> points to a <b>NULL</b> value and the caller should delete the source item.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
When the item being moved is a folder, the caller should convert a move operation into a copy and delete operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SAME_DEVICE</b></dt>
</dl>
</td>
<td width="60%">
The caller should convert a move operation into a copy and delete operation. This error is seen as <code>HRESULT_FROM_WIN32(ERROR_NOT_SAME_DEVICE)</code>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
When moving a folder, the caller should convert the move operation into a copy and delete operation. The destination item must support <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransferdestination">ITransferDestination</a>. This error is seen as <code>HRESULT_FROM_WIN32(ERROR_FILE_EXISTS)</code>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ALREADY_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
When moving a folder, the caller should convert the move operation into a copy and delete operation. The destination item must support <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransferdestination">ITransferDestination</a>. This error is seen as <code>HRESULT_FROM_WIN32(ERROR_ALREADY_EXISTS)</code>.

</td>
</tr>
</table>