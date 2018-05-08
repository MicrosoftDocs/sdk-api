---
UID: NN:comsvcs.SecurityProperty
title: SecurityProperty
author: windows-driver-content
description: Retrieves information about the current object's original caller and direct caller.
old-location: cos\securityproperty.htm
old-project: cossdk
ms.assetid: e4eb8e83-3510-4c2c-8b9c-563bfcbf48b3
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: SecurityProperty, SecurityProperty interface [COM+], SecurityProperty interface [COM+],described, _cos_SecurityProperty, comsvcs/SecurityProperty, cos.securityproperty
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
-	SecurityProperty
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# SecurityProperty interface


## -description


Retrieves information about the current object's original caller and direct caller.

The preferred way to obtain information about an object's callers is to use the <a href="https://msdn.microsoft.com/e8ac05fb-6665-4e57-b64e-82d9799d29d4">SecurityCallContext</a> class instead of the <b>SecurityProperty</b> interface.

<b>SecurityProperty</b> and <a href="https://msdn.microsoft.com/116715a5-a3e1-48aa-b155-107ea330b7ee">ISecurityProperty</a> provide the same functionality, but unlike <b>ISecurityProperty</b>, <b>SecurityProperty</b> is compatible with Automation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">SecurityProperty</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>SecurityProperty</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>SecurityProperty</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/451e073f-8dba-459a-92f3-4e9f1128a2c6">GetDirectCallerName</a>
</td>
<td align="left" width="63%">
Retrieves the user name associated with the external process that called the currently executing method.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/26619719-bcca-4776-9580-edc541e6b821">GetDirectCreatorName</a>
</td>
<td align="left" width="63%">
Retrieves the user name associated with the current object's immediate (out-of-process) creator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ca57950c-3079-42bd-a832-9b7753c61a39">GetOriginalCallerName</a>
</td>
<td align="left" width="63%">
Retrieves the user name associated with the base process that initiated the sequence of calls from which the call into the current object originated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/403f0f36-f386-4eeb-905a-e04c5699db9b">GetOriginalCreatorName</a>
</td>
<td align="left" width="63%">
Retrieves the user name associated with the original base process that initiated the activity in which the current object is executing.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/116715a5-a3e1-48aa-b155-107ea330b7ee">ISecurityProperty</a>



<a href="https://msdn.microsoft.com/09a17e57-7224-43bc-93c7-16ab95ca2517">ObjectContext</a>



<a href="https://msdn.microsoft.com/6117970c-5dbd-485e-978e-3aa96e42b359">Programmatic Component Security</a>
 

 

