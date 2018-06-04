---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

