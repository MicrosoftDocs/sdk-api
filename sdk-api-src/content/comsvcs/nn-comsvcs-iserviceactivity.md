---
UID: NN:comsvcs.IServiceActivity
title: IServiceActivity
author: windows-sdk-content
description: Used to call the batch work that is submitted through the activity created by CoCreateActivity.
old-location: cos\iserviceactivity.htm
tech.root: cossdk
ms.assetid: 005bf0ec-f5a7-41a3-85b3-07f79f26af27
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IServiceActivity, IServiceActivity interface [COM+], IServiceActivity interface [COM+],described, _cos_IServiceActivity, comsvcs/IServiceActivity, cos.iserviceactivity
ms.prod: windows
ms.technology: windows-sdk
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


Used to call the batch work that is submitted through the activity created by <a href="https://msdn.microsoft.com/en-us/library/ms679553(v=VS.85).aspx">CoCreateActivity</a>.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IServiceActivity</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IServiceActivity</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/ms679229(v=VS.85).aspx">AsynchronousCall</a>
</td>
<td align="left" width="63%">
Performs the user-defined work asynchronously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms680314(v=VS.85).aspx">BindToCurrentThread</a>
</td>
<td align="left" width="63%">
Binds the user-defined batch work to the current thread.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms686691(v=VS.85).aspx">SynchronousCall</a>
</td>
<td align="left" width="63%">
Performs the user-defined work synchronously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms687124(v=VS.85).aspx">UnbindFromThread</a>
</td>
<td align="left" width="63%">
Unbinds the user-defined batch work from the thread on which it is running.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a>



<a href="https://msdn.microsoft.com/en-us/library/ms679553(v=VS.85).aspx">CoCreateActivity</a>



<a href="https://msdn.microsoft.com/en-us/library/ms683598(v=VS.85).aspx">IAsyncErrorNotify</a>



<a href="https://msdn.microsoft.com/en-us/library/ms684294(v=VS.85).aspx">IServiceCall</a>



<a href="https://msdn.microsoft.com/en-us/library/ms683642(v=VS.85).aspx">IServiceThreadPoolConfig</a>
 

 

