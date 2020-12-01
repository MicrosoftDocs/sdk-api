---
UID: NF:shobjidl_core.ITransferSource.RecycleItem
title: ITransferSource::RecycleItem (shobjidl_core.h)
description: Recycle the item into the provided recycle location and return the item in its new location.
helpviewer_keywords: ["ITransferSource interface [Windows Shell]","RecycleItem method","ITransferSource.RecycleItem","ITransferSource::RecycleItem","RecycleItem","RecycleItem method [Windows Shell]","RecycleItem method [Windows Shell]","ITransferSource interface","_shell_ITransferSource_RecycleItem","shell.ITransferSource_RecycleItem","shobjidl_core/ITransferSource::RecycleItem"]
old-location: shell\ITransferSource_RecycleItem.htm
tech.root: shell
ms.assetid: ee99a1ff-1a3e-46a4-82c6-df5f6c26c396
ms.date: 12/05/2018
ms.keywords: ITransferSource interface [Windows Shell],RecycleItem method, ITransferSource.RecycleItem, ITransferSource::RecycleItem, RecycleItem, RecycleItem method [Windows Shell], RecycleItem method [Windows Shell],ITransferSource interface, _shell_ITransferSource_RecycleItem, shell.ITransferSource_RecycleItem, shobjidl_core/ITransferSource::RecycleItem
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
 - ITransferSource::RecycleItem
 - shobjidl_core/ITransferSource::RecycleItem
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
 - ITransferSource.RecycleItem
---

# ITransferSource::RecycleItem


## -description

Recycle the item into the provided recycle location and return the item in its new location.

## -parameters

### -param psiSource [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> to be recycled.

### -param psiParentDest [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> of the recycle location (the new parent of the item).

### -param flags [in]

Type: <b><a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_transfer_source_flags">TRANSFER_SOURCE_FLAGS</a></b>

The flags that control the file operation. One or more of the <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_transfer_source_flags">TRANSFER_SOURCE_FLAGS</a> constants.

### -param ppsiNewDest [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>**</b>

When the method returns, contains the address of a pointer to the recycled <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>.

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
<dt><b>COPYENGINE_S_DONT_PROCESS_CHILDREN</b></dt>
</dl>
</td>
<td width="60%">
Children items should not be processed.

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