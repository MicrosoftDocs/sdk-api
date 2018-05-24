---
UID: NF:shobjidl_core.ITransferAdviseSink.ConfirmEncryptionLoss
title: ITransferAdviseSink::ConfirmEncryptionLoss
author: windows-driver-content
description: Displays a message to the user confirming that loss of encryption is acceptable for this operation.
old-location: shell\ITransferAdviseSink_ConfirmEncryptionLoss.htm
old-project: shell
ms.assetid: 6c6c6c6a-9eb0-43dd-a51f-cdbe6d538652
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: ConfirmEncryptionLoss, ConfirmEncryptionLoss method [Windows Shell], ConfirmEncryptionLoss method [Windows Shell],ITransferAdviseSink interface, ITransferAdviseSink interface [Windows Shell],ConfirmEncryptionLoss method, ITransferAdviseSink.ConfirmEncryptionLoss, ITransferAdviseSink::ConfirmEncryptionLoss, _shell_ITransferAdviseSink_ConfirmEncryptionLoss, shell.ITransferAdviseSink_ConfirmEncryptionLoss, shobjidl_core/ITransferAdviseSink::ConfirmEncryptionLoss
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
-	ITransferAdviseSink.ConfirmEncryptionLoss
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# ITransferAdviseSink::ConfirmEncryptionLoss


## -description


Displays a message to the user confirming that loss of encryption is acceptable for this operation.


## -parameters




### -param psiSource

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> of the file in which encryption information will be lost.


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
 



