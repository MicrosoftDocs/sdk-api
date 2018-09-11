---
UID: NN:comsvcs.ISecurityProperty
title: ISecurityProperty
author: windows-sdk-content
description: Determines the security identifier of the current object's original caller or direct caller. However, the preferred way to get information about an object's callers is to use the ISecurityCallContext interface.
old-location: cos\isecurityproperty.htm
tech.root: cossdk
ms.assetid: 116715a5-a3e1-48aa-b155-107ea330b7ee
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ISecurityProperty, ISecurityProperty interface [COM+], ISecurityProperty interface [COM+],described, _cos_ISecurityProperty, comsvcs/ISecurityProperty, cos.isecurityproperty
ms.prod: windows
ms.technology: windows-sdk
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ISecurityProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISecurityProperty interface


## -description


Determines the security identifier of the current object's original caller or direct caller. However, the preferred way to get information about an object's callers is to use the <a href="https://msdn.microsoft.com/en-us/library/ms686495(v=VS.85).aspx">ISecurityCallContext</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISecurityProperty</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>ISecurityProperty</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/ms687557(v=VS.85).aspx">GetDirectCallerSID</a>
</td>
<td align="left" width="63%">
Retrieves the security identifier of the external process that called the currently executing method.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms686487(v=VS.85).aspx">GetDirectCreatorSID</a>
</td>
<td align="left" width="63%">
In MTS 2.0, this method retrieves the security identifier of the external process that directly created the current object. Do not use this method in COM+.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms687631(v=VS.85).aspx">GetOriginalCallerSID</a>
</td>
<td align="left" width="63%">
Retrieves the security identifier of the base process that initiated the call sequence from which the current method was called.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms681712(v=VS.85).aspx">GetOriginalCreatorSID</a>
</td>
<td align="left" width="63%">
In MTS 2.0, this method retrieves the security identifier of the base process that initiated the activity in which the current object is executing. Do not use this method in COM+.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms681321(v=VS.85).aspx">ReleaseSID</a>
</td>
<td align="left" width="63%">
Releases the security identifier returned by one of the other <b>ISecurityProperty</b> methods.


</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms686495(v=VS.85).aspx">ISecurityCallContext</a>



<a href="https://msdn.microsoft.com/en-us/library/ms681779(v=VS.85).aspx">Programmatic Component Security</a>
 

 

