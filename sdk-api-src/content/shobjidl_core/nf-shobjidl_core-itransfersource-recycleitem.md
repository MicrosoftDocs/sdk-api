---
UID: NF:shobjidl_core.ITransferSource.RecycleItem
title: ITransferSource::RecycleItem
author: windows-driver-content
description: Recycle the item into the provided recycle location and return the item in its new location.
old-location: shell\ITransferSource_RecycleItem.htm
old-project: shell
ms.assetid: ee99a1ff-1a3e-46a4-82c6-df5f6c26c396
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: ITransferSource interface [Windows Shell],RecycleItem method, ITransferSource.RecycleItem, ITransferSource::RecycleItem, RecycleItem, RecycleItem method [Windows Shell], RecycleItem method [Windows Shell],ITransferSource interface, _shell_ITransferSource_RecycleItem, shell.ITransferSource_RecycleItem, shobjidl_core/ITransferSource::RecycleItem
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	shobjidl_core.h
api_name:
-	ITransferSource.RecycleItem
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# ITransferSource::RecycleItem


## -description


Recycle the item into the provided recycle location and return the item in its new location.


## -parameters




### -param psiSource [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> to be recycled.


### -param psiParentDest [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> of the recycle location (the new parent of the item).


### -param flags




### -param ppsiNewDest [out]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>**</b>

When the method returns, contains the address of a pointer to the recycled <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>.


#### - dwDeleteFlags [in]

Type: <b><a href="https://msdn.microsoft.com/8a3da00a-1d96-444d-acbe-9327620b8d24">TRANSFER_SOURCE_FLAGS</a></b>

The flags that control the file operation. One or more of the <a href="https://msdn.microsoft.com/8a3da00a-1d96-444d-acbe-9327620b8d24">TRANSFER_SOURCE_FLAGS</a> constants.


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
 



