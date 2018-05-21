---
UID: NN:comsvcs.ISecurityProperty
title: ISecurityProperty
author: windows-driver-content
description: Determines the security identifier of the current object's original caller or direct caller. However, the preferred way to get information about an object's callers is to use the ISecurityCallContext interface.
old-location: cos\isecurityproperty.htm
old-project: cossdk
ms.assetid: 116715a5-a3e1-48aa-b155-107ea330b7ee
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: ISecurityProperty, ISecurityProperty interface [COM+], ISecurityProperty interface [COM+],described, _cos_ISecurityProperty, comsvcs/ISecurityProperty, cos.isecurityproperty
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
-	ISecurityProperty
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ISecurityProperty interface


## -description


Determines the security identifier of the current object's original caller or direct caller. However, the preferred way to get information about an object's callers is to use the <a href="https://msdn.microsoft.com/cd96ef31-784f-40fa-beb5-92a88823326b">ISecurityCallContext</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISecurityProperty</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISecurityProperty</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISecurityProperty</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e322df62-25a4-40a3-9b80-da468a265162">GetDirectCallerSID</a>
</td>
<td align="left" width="63%">
Retrieves the security identifier of the external process that called the currently executing method.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cd06e71b-563a-45d2-91fb-f57375016dc3">GetDirectCreatorSID</a>
</td>
<td align="left" width="63%">
In MTS 2.0, this method retrieves the security identifier of the external process that directly created the current object. Do not use this method in COM+.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e8700635-94cb-4d1a-9325-f93d00c5181f">GetOriginalCallerSID</a>
</td>
<td align="left" width="63%">
Retrieves the security identifier of the base process that initiated the call sequence from which the current method was called.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/599b0773-feee-4e3d-a23b-cc2c294f49f9">GetOriginalCreatorSID</a>
</td>
<td align="left" width="63%">
In MTS 2.0, this method retrieves the security identifier of the base process that initiated the activity in which the current object is executing. Do not use this method in COM+.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/572bf3fd-eb85-40de-b607-26b77b9d9cf8">ReleaseSID</a>
</td>
<td align="left" width="63%">
Releases the security identifier returned by one of the other <b>ISecurityProperty</b> methods.


</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/cd96ef31-784f-40fa-beb5-92a88823326b">ISecurityCallContext</a>



<a href="https://msdn.microsoft.com/6117970c-5dbd-485e-978e-3aa96e42b359">Programmatic Component Security</a>
 

 

