---
UID: NN:comsvcs.IServiceInheritanceConfig
title: IServiceInheritanceConfig
author: windows-driver-content
description: Determines whether to construct a new context based on the current context or to create a new context based solely on the information in CServiceConfig.
old-location: cos\iserviceinheritanceconfig.htm
old-project: cossdk
ms.assetid: 8bb95aef-7470-43cc-941d-2105cdf48f37
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IServiceInheritanceConfig, IServiceInheritanceConfig interface [COM+], IServiceInheritanceConfig interface [COM+],described, _cos_IServiceInheritanceConfig, comsvcs/IServiceInheritanceConfig, cos.iserviceinheritanceconfig
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	IServiceInheritanceConfig
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IServiceInheritanceConfig interface


## -description


Determines whether to construct a new context based on the current context or to create a new context based solely on the information in <a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a>. A new context that is based on the current context can be modified by calls to the other interfaces of <a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a>. 



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IServiceInheritanceConfig</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IServiceInheritanceConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IServiceInheritanceConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/05009c50-1d39-46f7-b549-281342d07f5b">ContainingContextTreatment</a>
</td>
<td align="left" width="63%">
Determines whether the containing context is based on the current context.


</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a>
 

 

