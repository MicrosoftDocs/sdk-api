---
UID: NN:shobjidl_core.ITransferAdviseSink
title: ITransferAdviseSink (shobjidl_core.h)
description: Exposes methods supporting status collection and failure information.
helpviewer_keywords: ["ITransferAdviseSink","ITransferAdviseSink interface [Windows Shell]","ITransferAdviseSink interface [Windows Shell]","described","_shell_ITransferAdviseSink","shell.ITransferAdviseSink","shobjidl_core/ITransferAdviseSink"]
old-location: shell\ITransferAdviseSink.htm
tech.root: shell
ms.assetid: 70866a03-2b22-4518-a9e6-2f06edaa4b5d
ms.date: 12/05/2018
ms.keywords: ITransferAdviseSink, ITransferAdviseSink interface [Windows Shell], ITransferAdviseSink interface [Windows Shell],described, _shell_ITransferAdviseSink, shell.ITransferAdviseSink, shobjidl_core/ITransferAdviseSink
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
 - ITransferAdviseSink
 - shobjidl_core/ITransferAdviseSink
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
 - ITransferAdviseSink
---

# ITransferAdviseSink interface


## -description

Exposes methods supporting status collection and failure information.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITransferAdviseSink</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITransferAdviseSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITransferAdviseSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransferadvisesink-confirmencryptionloss">ConfirmEncryptionLoss</a>
</td>
<td align="left" width="63%">
Displays a message to the user confirming that loss of encryption is acceptable for this operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransferadvisesink-confirmoverwrite">ConfirmOverwrite</a>
</td>
<td align="left" width="63%">
Displays a message to the user confirming that overwriting existing items is acceptable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransferadvisesink-filefailure">FileFailure</a>
</td>
<td align="left" width="63%">
Called when there is a failure and user interaction is needed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransferadvisesink-propertyfailure">PropertyFailure</a>
</td>
<td align="left" width="63%">
Called when there is a failure that involves file properties and user interaction is needed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransferadvisesink-substreamfailure">SubStreamFailure</a>
</td>
<td align="left" width="63%">
Called when there is a failure that involves secondary streams and user interaction is needed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransferadvisesink-updateprogress">UpdateProgress</a>
</td>
<td align="left" width="63%">
Updates the transfer progress status in the UI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransferadvisesink-updatetransferstate">UpdateTransferState</a>
</td>
<td align="left" width="63%">
Updates the transfer state.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransfersource">ITransferSource</a>