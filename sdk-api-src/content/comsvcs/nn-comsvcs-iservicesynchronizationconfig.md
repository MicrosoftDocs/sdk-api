---
UID: NN:comsvcs.IServiceSynchronizationConfig
title: IServiceSynchronizationConfig
author: windows-sdk-content
description: Configures the synchronization for the work that is done when calling either CoCreateActivity or CoEnterServiceDomain.
old-location: cos\iservicesynchronizationconfig.htm
old-project: cossdk
ms.assetid: c4856738-66bf-4982-9440-83b72148c85c
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IServiceSynchronizationConfig, IServiceSynchronizationConfig interface [COM+], IServiceSynchronizationConfig interface [COM+],described, _cos_IServiceSynchronizationConfig, comsvcs/IServiceSynchronizationConfig, cos.iservicesynchronizationconfig
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TRACKING_COLL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IServiceSynchronizationConfig
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IServiceSynchronizationConfig interface


## -description


Configures the synchronization for the work that is done when calling either <a href="https://msdn.microsoft.com/3009eb4f-e3f3-497b-ba05-5b750d8a40d0">CoCreateActivity</a> or <a href="https://msdn.microsoft.com/84640b3b-1f43-4bec-abf6-c295cfb3da8b">CoEnterServiceDomain</a>.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IServiceSynchronizationConfig</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IServiceSynchronizationConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IServiceSynchronizationConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/83fe6958-6639-4468-a3f5-3322316ccbc4">ConfigureSynchronization</a>
</td>
<td align="left" width="63%">
Configures the synchronization for the enclosed work.


</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a>
 

 

