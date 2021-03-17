---
UID: NF:shobjidl_core.ITransferAdviseSink.ConfirmEncryptionLoss
title: ITransferAdviseSink::ConfirmEncryptionLoss (shobjidl_core.h)
description: Displays a message to the user confirming that loss of encryption is acceptable for this operation.
helpviewer_keywords: ["ConfirmEncryptionLoss","ConfirmEncryptionLoss method [Windows Shell]","ConfirmEncryptionLoss method [Windows Shell]","ITransferAdviseSink interface","ITransferAdviseSink interface [Windows Shell]","ConfirmEncryptionLoss method","ITransferAdviseSink.ConfirmEncryptionLoss","ITransferAdviseSink::ConfirmEncryptionLoss","_shell_ITransferAdviseSink_ConfirmEncryptionLoss","shell.ITransferAdviseSink_ConfirmEncryptionLoss","shobjidl_core/ITransferAdviseSink::ConfirmEncryptionLoss"]
old-location: shell\ITransferAdviseSink_ConfirmEncryptionLoss.htm
tech.root: shell
ms.assetid: 6c6c6c6a-9eb0-43dd-a51f-cdbe6d538652
ms.date: 12/05/2018
ms.keywords: ConfirmEncryptionLoss, ConfirmEncryptionLoss method [Windows Shell], ConfirmEncryptionLoss method [Windows Shell],ITransferAdviseSink interface, ITransferAdviseSink interface [Windows Shell],ConfirmEncryptionLoss method, ITransferAdviseSink.ConfirmEncryptionLoss, ITransferAdviseSink::ConfirmEncryptionLoss, _shell_ITransferAdviseSink_ConfirmEncryptionLoss, shell.ITransferAdviseSink_ConfirmEncryptionLoss, shobjidl_core/ITransferAdviseSink::ConfirmEncryptionLoss
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
 - ITransferAdviseSink::ConfirmEncryptionLoss
 - shobjidl_core/ITransferAdviseSink::ConfirmEncryptionLoss
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
 - ITransferAdviseSink.ConfirmEncryptionLoss
---

# ITransferAdviseSink::ConfirmEncryptionLoss


## -description

Displays a message to the user confirming that loss of encryption is acceptable for this operation.

## -parameters

### -param psiSource

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> of the file in which encryption information will be lost.

## -returns

Type: <b>HRESULT</b>

Returns one of the following specific Shell codes, or a system error code.

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
User responded "Yes" to the dialog. Copy continues without encryption.

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
<dt><b>COPYENGINE_S_PENDING</b></dt>
</dl>
</td>
<td width="60%">
Error has been queued and will display later. Operation on this file will be skipped.

</td>
</tr>
</table>