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

# IMTSActivity interface


## -description


<p class="CCE_Message">[<b>IMTSActivity</b> is available for use in the operating systems specified in the Requirements section. It may be altered of unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/005bf0ec-f5a7-41a3-85b3-07f79f26af27">IServiceActivity</a>.]

Submits batch work through the activity created by the <a href="https://msdn.microsoft.com/25ae1f2e-f937-4d06-9709-ded2fc8c5777">MTSCreateActivity</a> function.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMTSActivity</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMTSActivity</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMTSActivity</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ccbb96e8-9fb8-40b4-b027-432ba8c400c7">AsyncCall</a>
</td>
<td align="left" width="63%">
Performs the user-defined work asynchronously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/31f0c64c-275c-431c-b85e-6ee5f4318e1f">BindToCurrentThread</a>
</td>
<td align="left" width="63%">
Binds the batch work that is submitted using <a href="https://msdn.microsoft.com/ccbb96e8-9fb8-40b4-b027-432ba8c400c7">IMTSActivity::AsyncCall</a> or <a href="https://msdn.microsoft.com/4f69956b-fdb3-47c4-9a19-e9f39a8d5e06">IMTSActivity::SynchronousCall</a> to the current single-threaded apartment (STA).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4f69956b-fdb3-47c4-9a19-e9f39a8d5e06">SynchronousCall</a>
</td>
<td align="left" width="63%">
Performs the user-defined work synchronously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cb4c4f63-2a6e-4df7-8886-19d45e28d81a">UnbindFromThread</a>
</td>
<td align="left" width="63%">
Unbinds the batch work that is submitted using <a href="https://msdn.microsoft.com/ccbb96e8-9fb8-40b4-b027-432ba8c400c7">IMTSActivity::AsyncCall</a> or <a href="https://msdn.microsoft.com/4f69956b-fdb3-47c4-9a19-e9f39a8d5e06">IMTSActivity::SynchronousCall</a> from the thread on which it is running.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/410ed66e-db55-41e6-8f09-df4fe3aad3f2">IMTSCall::OnCall</a>



<a href="https://msdn.microsoft.com/005bf0ec-f5a7-41a3-85b3-07f79f26af27">IServiceActivity</a>



<a href="https://msdn.microsoft.com/25ae1f2e-f937-4d06-9709-ded2fc8c5777">MTSCreateActivity</a>
 

 

