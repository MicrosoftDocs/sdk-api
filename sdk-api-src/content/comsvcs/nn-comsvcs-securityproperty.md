---
UID: NN:comsvcs.SecurityProperty
title: SecurityProperty (comsvcs.h)
description: Retrieves information about the current object's original caller and direct caller.
helpviewer_keywords: ["SecurityProperty","SecurityProperty interface [COM+]","SecurityProperty interface [COM+]","described","_cos_SecurityProperty","comsvcs/SecurityProperty","cos.securityproperty"]
old-location: cos\securityproperty.htm
tech.root: cos
ms.assetid: e4eb8e83-3510-4c2c-8b9c-563bfcbf48b3
ms.date: 12/05/2018
ms.keywords: SecurityProperty, SecurityProperty interface [COM+], SecurityProperty interface [COM+],described, _cos_SecurityProperty, comsvcs/SecurityProperty, cos.securityproperty
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SecurityProperty
 - comsvcs/SecurityProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - SecurityProperty
---

# SecurityProperty interface


## -description

Retrieves information about the current object's original caller and direct caller.

The preferred way to obtain information about an object's callers is to use the <a href="/windows/desktop/cossdk/securitycallcontext">SecurityCallContext</a> class instead of the <b>SecurityProperty</b> interface.

<b>SecurityProperty</b> and <a href="/windows/desktop/api/comsvcs/nn-comsvcs-isecurityproperty">ISecurityProperty</a> provide the same functionality, but unlike <b>ISecurityProperty</b>, <b>SecurityProperty</b> is compatible with Automation.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">SecurityProperty</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>SecurityProperty</b> also has these types of members:
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
<a href="/windows/desktop/api/comsvcs/nf-comsvcs-securityproperty-getdirectcallername">GetDirectCallerName</a>
</td>
<td align="left" width="63%">
Retrieves the user name associated with the external process that called the currently executing method.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/comsvcs/nf-comsvcs-securityproperty-getdirectcreatorname">GetDirectCreatorName</a>
</td>
<td align="left" width="63%">
Retrieves the user name associated with the current object's immediate (out-of-process) creator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/comsvcs/nf-comsvcs-securityproperty-getoriginalcallername">GetOriginalCallerName</a>
</td>
<td align="left" width="63%">
Retrieves the user name associated with the base process that initiated the sequence of calls from which the call into the current object originated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/comsvcs/nf-comsvcs-securityproperty-getoriginalcreatorname">GetOriginalCreatorName</a>
</td>
<td align="left" width="63%">
Retrieves the user name associated with the original base process that initiated the activity in which the current object is executing.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-isecurityproperty">ISecurityProperty</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-objectcontext">ObjectContext</a>



<a href="/windows/desktop/cossdk/programmatic-component-security">Programmatic Component Security</a>