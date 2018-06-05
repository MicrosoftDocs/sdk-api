---
UID: NN:comsvcs.IServiceCall
title: IServiceCall
author: windows-sdk-content
description: Used to implement the batch work that is submitted through the activity created by CoCreateActivity.
old-location: cos\iservicecall.htm
old-project: cossdk
ms.assetid: 97532e29-3d1a-4a7c-8103-dd7ae2866a70
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IServiceCall, IServiceCall interface [COM+], IServiceCall interface [COM+],described, _cos_IServiceCall, comsvcs/IServiceCall, cos.iservicecall
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
-	IServiceCall
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IServiceCall interface


## -description


Used to implement the batch work that is submitted through the activity created by <a href="https://msdn.microsoft.com/3009eb4f-e3f3-497b-ba05-5b750d8a40d0">CoCreateActivity</a>.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IServiceCall</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IServiceCall</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IServiceCall</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0a2bb7ed-018f-4cb1-a1b2-27f6949dae39">OnCall</a>
</td>
<td align="left" width="63%">
Triggers the execution of the batch work implemented in this method.


</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3009eb4f-e3f3-497b-ba05-5b750d8a40d0">CoCreateActivity</a>



<a href="https://msdn.microsoft.com/870ab43a-c675-499b-a1e3-1f48176768c0">IAsyncErrorNotify</a>



<a href="https://msdn.microsoft.com/005bf0ec-f5a7-41a3-85b3-07f79f26af27">IServiceActivity</a>
 

 

