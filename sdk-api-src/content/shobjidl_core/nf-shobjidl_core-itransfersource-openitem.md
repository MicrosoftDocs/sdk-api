---
UID: NF:shobjidl_core.ITransferSource.OpenItem
title: ITransferSource::OpenItem (shobjidl_core.h)
description: Opens the item for copying. Returns an object that can be enumerated for resources (IShellItemResources).
helpviewer_keywords: ["ITransferSource interface [Windows Shell]","OpenItem method","ITransferSource.OpenItem","ITransferSource::OpenItem","OpenItem","OpenItem method [Windows Shell]","OpenItem method [Windows Shell]","ITransferSource interface","_shell_ITransferSource_OpenItem","shell.ITransferSource_OpenItem","shobjidl_core/ITransferSource::OpenItem"]
old-location: shell\ITransferSource_OpenItem.htm
tech.root: shell
ms.assetid: 8f051923-2798-43e9-8e8d-95eec5f618aa
ms.date: 12/05/2018
ms.keywords: ITransferSource interface [Windows Shell],OpenItem method, ITransferSource.OpenItem, ITransferSource::OpenItem, OpenItem, OpenItem method [Windows Shell], OpenItem method [Windows Shell],ITransferSource interface, _shell_ITransferSource_OpenItem, shell.ITransferSource_OpenItem, shobjidl_core/ITransferSource::OpenItem
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
 - ITransferSource::OpenItem
 - shobjidl_core/ITransferSource::OpenItem
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
 - ITransferSource.OpenItem
---

# ITransferSource::OpenItem


## -description

Opens the item for copying. Returns an object that can be enumerated for resources (<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemresources">IShellItemResources</a>).

## -parameters

### -param psi [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> to be opened.

### -param flags [in]

Type: <b><a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_transfer_source_flags">TRANSFER_SOURCE_FLAGS</a></b>

The flags that control the file operation. One or more of the <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_transfer_source_flags">TRANSFER_SOURCE_FLAGS</a> constants.

### -param riid [out]

Type: <b>REFIID</b>

A reference to the IID (the interface ID or GUID) of the interface to return in <i>ppv</i>.  This should be an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemresources">IShellItemResources</a> or an interface derived from <b>IShellItemResources</b>.

### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the address of a pointer to the interface specified by <i>riid</i>.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or one of the following specific Shell codes, or a system error code.

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