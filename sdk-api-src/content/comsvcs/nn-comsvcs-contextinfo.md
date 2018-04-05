---
UID: NN:comsvcs.ContextInfo
title: ContextInfo
author: windows-driver-content
description: Retrieves transaction, activity, and context information on the current context object. Using the methods of this interface, you can retrieve relevant information contained within an object context.
old-location: cos\contextinfo.htm
old-project: cossdk
ms.assetid: ef8d7ef7-fae4-4a20-80fb-18f5daa9b564
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: ContextInfo, ContextInfo interface [COM+], ContextInfo interface [COM+], described, _cos_ContextInfo, comsvcs/ContextInfo, cos.contextinfo
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
-	ContextInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ContextInfo interface


## -description


Retrieves transaction, activity, and context information on the current context object. Using the methods of this interface, you can retrieve relevant information contained within an object context.

<b>ContextInfo</b> and <a href="https://msdn.microsoft.com/76dcc6f3-f840-4672-bba9-038c1249a306">IObjectContextInfo</a> provide the same functionality, but unlike <b>IObjectContextInfo</b>, <b>ContextInfo</b> is compatible with Automation.

In COM+ 1.5, released with Windows XP, the <b>ContextInfo</b> interface is superseded by the <a href="https://msdn.microsoft.com/06954cc5-19a7-4bae-ac30-94dcdc35d15d">ContextInfo2</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ContextInfo</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ContextInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ContextInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1bc87f84-fc98-4ea3-b137-2a88a25d290d">GetActivityId</a>
</td>
<td align="left" width="63%">
Retrieves the activity identifier associated with the object context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/92566450-8351-49e7-94e1-35a331195322">GetContextId</a>
</td>
<td align="left" width="63%">
Retrieves the unique identifier of this object context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9922f2a3-9b2e-4bfe-8a9a-a17c0628439e">GetTransaction</a>
</td>
<td align="left" width="63%">
Retrieves the object context's transaction object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9eb77a13-14f0-4d45-a6de-4ae28d6bcac4">GetTransactionId</a>
</td>
<td align="left" width="63%">
Retrieves the transaction identifier associated with the object context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/587805a4-6713-40be-83b6-5c772b5396cf">IsInTransaction</a>
</td>
<td align="left" width="63%">
Indicates whether the current object is executing in a transaction.


</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/50ccf75e-2652-4254-a771-af83cc9248b3">COM+ Contexts and Threading Models</a>



<a href="https://msdn.microsoft.com/9395bc9a-dfe5-428a-839f-1c4ad090f636">IObjectContext</a>



<a href="https://msdn.microsoft.com/76dcc6f3-f840-4672-bba9-038c1249a306">IObjectContextInfo</a>



<a href="https://msdn.microsoft.com/09a17e57-7224-43bc-93c7-16ab95ca2517">ObjectContext</a>
 

 

