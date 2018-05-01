---
UID: NN:comsvcs.IGetSecurityCallContext
title: IGetSecurityCallContext
author: windows-driver-content
description: Retrieves a reference to an object created from the SecurityCallContext class that is associated with the current call.
old-location: cos\igetsecuritycallcontext.htm
old-project: cossdk
ms.assetid: 7be988b7-b144-4b8f-b8d3-b0700b564df3
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: IGetSecurityCallContext, IGetSecurityCallContext interface [COM+], IGetSecurityCallContext interface [COM+], described, _cos_IGetSecurityCallContext, comsvcs/IGetSecurityCallContext, cos.igetsecuritycallcontext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
-	IGetSecurityCallContext
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IGetSecurityCallContext interface


## -description


Retrieves a reference to an object created from the <a href="https://msdn.microsoft.com/e8ac05fb-6665-4e57-b64e-82d9799d29d4">SecurityCallContext</a> class that is associated with the current call.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGetSecurityCallContext</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IGetSecurityCallContext</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IGetSecurityCallContext</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6a386cf6-1f75-4915-8c89-e453c4ebdab8">GetSecurityClassContext</a>
</td>
<td align="left" width="63%">
Retrieves a reference to an object created from the <a href="https://msdn.microsoft.com/e8ac05fb-6665-4e57-b64e-82d9799d29d4">SecurityCallContext</a> class that is associated with the current call.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b82e32c0-840d-402e-90d5-ff678c51faf1">CoGetCallContext</a>



<a href="https://msdn.microsoft.com/cd96ef31-784f-40fa-beb5-92a88823326b">ISecurityCallContext</a>



<a href="https://msdn.microsoft.com/e8ac05fb-6665-4e57-b64e-82d9799d29d4">SecurityCallContext</a>
 

 

