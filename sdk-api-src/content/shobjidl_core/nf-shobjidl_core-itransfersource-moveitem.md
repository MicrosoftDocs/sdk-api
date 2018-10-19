---
UID: NF:shobjidl_core.ITransferSource.MoveItem
title: ITransferSource::MoveItem
author: windows-sdk-content
description: Moves the item within the volume/namespace, returning the IShellItem in its new location.
old-location: shell\ITransferSource_MoveItem.htm
tech.root: shell
ms.assetid: de59291c-12ad-4639-bc10-d8416a979eb7
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: ITransferSource interface [Windows Shell],MoveItem method, ITransferSource.MoveItem, ITransferSource::MoveItem, MoveItem, MoveItem method [Windows Shell], MoveItem method [Windows Shell],ITransferSource interface, _shell_ITransferSource_MoveItem, shell.ITransferSource_MoveItem, shobjidl_core/ITransferSource::MoveItem
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - ITransferSource.MoveItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITransferSource::MoveItem


## -description


Moves the item within the volume/namespace, returning the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> in its new location.


## -parameters




### -param psi [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> to be moved.


### -param psiParentDst [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> that represents the new parent item at the destination.


### -param pszNameDst [in]

Type: <b>LPCWSTR</b>

Pointer to a null-terminated buffer that contains the destination path.


### -param flags

TBD


### -param ppsiNew [out]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>**</b>

When this method returns successfully, contains an address of a pointer to the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> in its new location.


#### - dwFlags

Type: <b><a href="https://msdn.microsoft.com/8a3da00a-1d96-444d-acbe-9327620b8d24">TRANSFER_SOURCE_FLAGS</a></b>

Flags that control the file operation. One or more of the <a href="https://msdn.microsoft.com/8a3da00a-1d96-444d-acbe-9327620b8d24">TRANSFER_SOURCE_FLAGS</a> constants.


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
When moving a folder, the caller should convert the move operation into a copy and delete operation. The destination item must support <a href="https://msdn.microsoft.com/8d0049e0-e227-40ae-a282-cdc17f227e24">ITransferDestination</a>. This error is seen as <code>HRESULT_FROM_WIN32(ERROR_FILE_EXISTS)</code>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ALREADY_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
When moving a folder, the caller should convert the move operation into a copy and delete operation. The destination item must support <a href="https://msdn.microsoft.com/8d0049e0-e227-40ae-a282-cdc17f227e24">ITransferDestination</a>. This error is seen as <code>HRESULT_FROM_WIN32(ERROR_ALREADY_EXISTS)</code>.

</td>
</tr>
</table>
 



