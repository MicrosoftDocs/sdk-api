---
UID: NN:comsvcs.ContextInfo2
title: ContextInfo2
author: windows-driver-content
description: Provides additional information about an object's context, supplementing the information that is available through the ContextInfo interface.
old-location: cos\contextinfo2.htm
old-project: cossdk
ms.assetid: 06954cc5-19a7-4bae-ac30-94dcdc35d15d
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: ContextInfo2, ContextInfo2 interface [COM+], ContextInfo2 interface [COM+],described, _cos_ContextInfo2, comsvcs/ContextInfo2, cos.contextinfo2
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
-	ContextInfo2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ContextInfo2 interface


## -description


 Provides additional information about an object's context, supplementing the information that is available through the <a href="https://msdn.microsoft.com/ef8d7ef7-fae4-4a20-80fb-18f5daa9b564">ContextInfo</a> interface.

<b>ContextInfo2</b> and <a href="https://msdn.microsoft.com/21e078d2-ba93-4118-b1d1-3b4b6e0e28a4">IObjectContextInfo2</a> provide the same functionality, but unlike <b>IObjectContextInfo2</b>, <b>ContextInfo2</b> is compatible with Automation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ContextInfo2</b> interface inherits from <a href="https://msdn.microsoft.com/ef8d7ef7-fae4-4a20-80fb-18f5daa9b564">ContextInfo</a>. <b>ContextInfo2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ContextInfo2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9fc5cffe-a532-4084-8b6c-9812a5b117b2">GetApplicationId</a>
</td>
<td align="left" width="63%">
 Retrieves the GUID of the application of the current object context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/77149329-db3a-4ff4-a522-c290c2d0a915">GetApplicationInstanceId</a>
</td>
<td align="left" width="63%">
Retrieves the GUID of the application instance of the current object context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b4cda75d-a4f3-404e-965a-9c1487946ee1">GetPartitionId</a>
</td>
<td align="left" width="63%">
Retrieves the GUID of the COM+ partition of the current object context.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/50ccf75e-2652-4254-a771-af83cc9248b3">COM+ Contexts and Threading Models</a>



<a href="https://msdn.microsoft.com/fd22a64c-f2d8-48af-86e1-985e21b0f8fa">COM+ Partitions</a>



<a href="https://msdn.microsoft.com/ef8d7ef7-fae4-4a20-80fb-18f5daa9b564">ContextInfo</a>



<a href="https://msdn.microsoft.com/9395bc9a-dfe5-428a-839f-1c4ad090f636">IObjectContext</a>



<a href="https://msdn.microsoft.com/21e078d2-ba93-4118-b1d1-3b4b6e0e28a4">IObjectContextInfo2</a>



<a href="https://msdn.microsoft.com/09a17e57-7224-43bc-93c7-16ab95ca2517">ObjectContext</a>
 

 

