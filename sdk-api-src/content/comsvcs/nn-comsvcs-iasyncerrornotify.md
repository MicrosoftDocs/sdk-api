---
UID: NN:comsvcs.IAsyncErrorNotify
title: IAsyncErrorNotify
author: windows-driver-content
description: Used to implement error trapping on the asynchronous batch work that is submitted through the activity created by CoCreateActivity.
old-location: cos\iasyncerrornotify.htm
old-project: cossdk
ms.assetid: 870ab43a-c675-499b-a1e3-1f48176768c0
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: IAsyncErrorNotify, IAsyncErrorNotify interface [COM+], IAsyncErrorNotify interface [COM+], described, _cos_IAsyncErrorNotify, comsvcs/IAsyncErrorNotify, cos.iasyncerrornotify
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	IAsyncErrorNotify
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAsyncErrorNotify interface


## -description


Used to implement error trapping on the asynchronous batch work that is submitted through the activity created by <a href="https://msdn.microsoft.com/3009eb4f-e3f3-497b-ba05-5b750d8a40d0">CoCreateActivity</a>.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAsyncErrorNotify</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAsyncErrorNotify</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAsyncErrorNotify</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a48d7733-bbcb-4c03-b265-f112e24c07d9">OnError</a>
</td>
<td align="left" width="63%">
Called by COM+ when an error occurs in your asynchronous batch work.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3009eb4f-e3f3-497b-ba05-5b750d8a40d0">CoCreateActivity</a>



<a href="https://msdn.microsoft.com/005bf0ec-f5a7-41a3-85b3-07f79f26af27">IServiceActivity</a>



<a href="https://msdn.microsoft.com/97532e29-3d1a-4a7c-8103-dd7ae2866a70">IServiceCall</a>
 

 

