---
UID: NN:shobjidl_core.ITransferAdviseSink
title: ITransferAdviseSink (shobjidl_core.h)
author: windows-sdk-content
description: Exposes methods supporting status collection and failure information.
old-location: shell\ITransferAdviseSink.htm
tech.root: shell
ms.assetid: 70866a03-2b22-4518-a9e6-2f06edaa4b5d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITransferAdviseSink, ITransferAdviseSink interface [Windows Shell], ITransferAdviseSink interface [Windows Shell],described, _shell_ITransferAdviseSink, shell.ITransferAdviseSink, shobjidl_core/ITransferAdviseSink
ms.topic: interface
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
 - ITransferAdviseSink
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITransferAdviseSink interface


## -description


Exposes methods supporting status collection and failure information.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITransferAdviseSink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITransferAdviseSink</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/6c6c6c6a-9eb0-43dd-a51f-cdbe6d538652">ConfirmEncryptionLoss</a>
</td>
<td align="left" width="63%">
Displays a message to the user confirming that loss of encryption is acceptable for this operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1c7705c5-1a56-47c2-9b9b-3f72a4323cd7">ConfirmOverwrite</a>
</td>
<td align="left" width="63%">
Displays a message to the user confirming that overwriting existing items is acceptable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4adc4e9d-f1d1-438c-bae3-23d1259453a6">FileFailure</a>
</td>
<td align="left" width="63%">
Called when there is a failure and user interaction is needed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c43cb166-6edf-4c45-93c1-16cb9b5c2d30">PropertyFailure</a>
</td>
<td align="left" width="63%">
Called when there is a failure that involves file properties and user interaction is needed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4cca3bc0-45c6-40ee-8050-7035faa1e601">SubStreamFailure</a>
</td>
<td align="left" width="63%">
Called when there is a failure that involves secondary streams and user interaction is needed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/931029e8-48ff-4d24-8818-57b7103fffdf">UpdateProgress</a>
</td>
<td align="left" width="63%">
Updates the transfer progress status in the UI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/37e830b0-a426-4a66-83c3-108f315f50ac">UpdateTransferState</a>
</td>
<td align="left" width="63%">
Updates the transfer state.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/341966d4-f9cf-457d-97ef-8e6107544283">ITransferSource</a>
 

 

