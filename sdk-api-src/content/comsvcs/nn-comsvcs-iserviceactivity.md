---
UID: NN:comsvcs.IServiceActivity
title: IServiceActivity
author: windows-sdk-content
description: Used to call the batch work that is submitted through the activity created by CoCreateActivity.
old-location: cos\iserviceactivity.htm
tech.root: cossdk
ms.assetid: 005bf0ec-f5a7-41a3-85b3-07f79f26af27
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IServiceActivity, IServiceActivity interface [COM+], IServiceActivity interface [COM+],described, _cos_IServiceActivity, comsvcs/IServiceActivity, cos.iserviceactivity
ms.topic: interface
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - ComSvcs.h
api_name:
 - IServiceActivity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IServiceActivity interface


## -description


Used to call the batch work that is submitted through the activity created by <a href="https://msdn.microsoft.com/3009eb4f-e3f3-497b-ba05-5b750d8a40d0">CoCreateActivity</a>.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IServiceActivity</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IServiceActivity</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IServiceActivity</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1d81f2e6-9426-4733-bd1d-0b6ca087cc0a">AsynchronousCall</a>
</td>
<td align="left" width="63%">
Performs the user-defined work asynchronously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3d2b57fd-1714-4fdf-859c-9fdfb341dd5d">BindToCurrentThread</a>
</td>
<td align="left" width="63%">
Binds the user-defined batch work to the current thread.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d25e6942-7b1b-4b74-b711-2d0f513d0b38">SynchronousCall</a>
</td>
<td align="left" width="63%">
Performs the user-defined work synchronously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e28b413d-6e3e-4a1f-90ed-8b0ab88904aa">UnbindFromThread</a>
</td>
<td align="left" width="63%">
Unbinds the user-defined batch work from the thread on which it is running.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a>



<a href="https://msdn.microsoft.com/3009eb4f-e3f3-497b-ba05-5b750d8a40d0">CoCreateActivity</a>



<a href="https://msdn.microsoft.com/870ab43a-c675-499b-a1e3-1f48176768c0">IAsyncErrorNotify</a>



<a href="https://msdn.microsoft.com/97532e29-3d1a-4a7c-8103-dd7ae2866a70">IServiceCall</a>



<a href="https://msdn.microsoft.com/89c04fef-c6a0-4d73-a25a-a70b4b0f0bcf">IServiceThreadPoolConfig</a>
 

 

