---
UID: NN:comsvcs.IServiceThreadPoolConfig
title: IServiceThreadPoolConfig
author: windows-sdk-content
description: Configures the thread pool of the activity object that is returned by calling CoCreateActivity.
old-location: cos\iservicethreadpoolconfig.htm
tech.root: cossdk
ms.assetid: 89c04fef-c6a0-4d73-a25a-a70b4b0f0bcf
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IServiceThreadPoolConfig, IServiceThreadPoolConfig interface [COM+], IServiceThreadPoolConfig interface [COM+],described, _cos_IServiceThreadPoolConfig, comsvcs/IServiceThreadPoolConfig, cos.iservicethreadpoolconfig
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
 - IServiceThreadPoolConfig
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IServiceThreadPoolConfig interface


## -description


Configures the thread pool of the activity object that is returned by calling <a href="https://msdn.microsoft.com/3009eb4f-e3f3-497b-ba05-5b750d8a40d0">CoCreateActivity</a>. 



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IServiceThreadPoolConfig</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IServiceThreadPoolConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IServiceThreadPoolConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eba8b4fc-aee7-4ba5-8e0e-b74ce9d25a86">SelectThreadPool</a>
</td>
<td align="left" width="63%">
Selects the thread pool in which the work submitted through the activity is to run.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9d2c4e6f-aa12-4874-a8e0-ca21a981b43f">SetBindingInfo</a>
</td>
<td align="left" width="63%">
Binds all work submitted by the activity to a single single-threaded apartment.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a>
 

 

