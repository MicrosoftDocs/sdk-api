---
UID: NN:comsvcs.ISecurityProperty
title: ISecurityProperty (comsvcs.h)
description: Determines the security identifier of the current object's original caller or direct caller. However, the preferred way to get information about an object's callers is to use the ISecurityCallContext interface.helpviewer_keywords: ["ISecurityProperty","ISecurityProperty interface [COM+]","ISecurityProperty interface [COM+]","described","_cos_ISecurityProperty","comsvcs/ISecurityProperty","cos.isecurityproperty"]
old-location: cos\isecurityproperty.htm
tech.root: cossdk
ms.assetid: 116715a5-a3e1-48aa-b155-107ea330b7ee
ms.date: 12/05/2018
ms.keywords: ISecurityProperty, ISecurityProperty interface [COM+], ISecurityProperty interface [COM+],described, _cos_ISecurityProperty, comsvcs/ISecurityProperty, cos.isecurityproperty
f1_keywords:
- comsvcs/ISecurityProperty
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISecurityProperty interface


## -description


Determines the security identifier of the current object's original caller or direct caller. However, the preferred way to get information about an object's callers is to use the <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-isecuritycallcontext">ISecurityCallContext</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISecurityProperty</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISecurityProperty</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-isecurityproperty-getdirectcallersid">GetDirectCallerSID</a>
</td>
<td align="left" width="63%">
Retrieves the security identifier of the external process that called the currently executing method.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-isecurityproperty-getdirectcreatorsid">GetDirectCreatorSID</a>
</td>
<td align="left" width="63%">
In MTS 2.0, this method retrieves the security identifier of the external process that directly created the current object. Do not use this method in COM+.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-isecurityproperty-getoriginalcallersid">GetOriginalCallerSID</a>
</td>
<td align="left" width="63%">
Retrieves the security identifier of the base process that initiated the call sequence from which the current method was called.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-isecurityproperty-getoriginalcreatorsid">GetOriginalCreatorSID</a>
</td>
<td align="left" width="63%">
In MTS 2.0, this method retrieves the security identifier of the base process that initiated the activity in which the current object is executing. Do not use this method in COM+.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-isecurityproperty-releasesid">ReleaseSID</a>
</td>
<td align="left" width="63%">
Releases the security identifier returned by one of the other <b>ISecurityProperty</b> methods.


</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-isecuritycallcontext">ISecurityCallContext</a>



<a href="https://docs.microsoft.com/windows/desktop/cossdk/programmatic-component-security">Programmatic Component Security</a>
 

 

