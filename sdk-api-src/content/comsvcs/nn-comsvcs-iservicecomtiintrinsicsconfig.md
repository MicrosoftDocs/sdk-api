---
UID: NN:comsvcs.IServiceComTIIntrinsicsConfig
title: IServiceComTIIntrinsicsConfig
author: windows-sdk-content
description: Configures the COM Transaction Integrator (COMTI) intrinsics for the work that is done when calling the CoCreateActivity or CoEnterServiceDomain function.
old-location: cos\iservicecomtiintrinsicsconfig.htm
old-project: cossdk
ms.assetid: dafa74f9-21fb-4495-911a-60183d36d83c
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IServiceComTIIntrinsicsConfig, IServiceComTIIntrinsicsConfig interface [COM+], IServiceComTIIntrinsicsConfig interface [COM+],described, _cos_IServiceComTIIntrinsicsConfig, comsvcs/IServiceComTIIntrinsicsConfig, cos.iservicecomtiintrinsicsconfig
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	IServiceComTIIntrinsicsConfig
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IServiceComTIIntrinsicsConfig interface


## -description


Configures the COM Transaction Integrator (COMTI) intrinsics for the work that is done when calling the <a href="https://msdn.microsoft.com/3009eb4f-e3f3-497b-ba05-5b750d8a40d0">CoCreateActivity</a> or <a href="https://msdn.microsoft.com/84640b3b-1f43-4bec-abf6-c295cfb3da8b">CoEnterServiceDomain</a> function. The COMTI eases the task of wrapping mainframe transactions and business logic as COM components.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IServiceComTIIntrinsicsConfig</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IServiceComTIIntrinsicsConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IServiceComTIIntrinsicsConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2e534123-6300-4da3-a220-ba0b41a7c9a2">ComTIIntrinsicsConfig</a>
</td>
<td align="left" width="63%">
Configures the COMTI intrinsics for the enclosed work.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a>
 

 

