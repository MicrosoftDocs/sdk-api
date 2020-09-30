---
UID: NN:certenroll.IPolicyQualifiers
title: IPolicyQualifiers (certenroll.h)
description: Defines methods and properties that enable you to manage a collection of IPolicyQualifier objects.
helpviewer_keywords: ["IPolicyQualifiers","IPolicyQualifiers interface [Security]","IPolicyQualifiers interface [Security]","described","certenroll/IPolicyQualifiers","security.ipolicyqualifiers"]
old-location: security\ipolicyqualifiers.htm
tech.root: security
ms.assetid: da8b6289-379e-4dff-b15a-b0967f245c3d
ms.date: 12/05/2018
ms.keywords: IPolicyQualifiers, IPolicyQualifiers interface [Security], IPolicyQualifiers interface [Security],described, certenroll/IPolicyQualifiers, security.ipolicyqualifiers
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: CertEnroll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPolicyQualifiers
 - certenroll/IPolicyQualifiers
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IPolicyQualifiers
---

# IPolicyQualifiers interface


## -description

The <b>IPolicyQualifiers</b> interface defines methods and properties that enable you to manage a collection of <a href="/windows/desktop/api/certenroll/nn-certenroll-ipolicyqualifier">IPolicyQualifier</a> objects.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPolicyQualifiers</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IPolicyQualifiers</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IPolicyQualifiers</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/certenroll/nf-certenroll-ipolicyqualifiers-add">Add</a>
</td>
<td align="left" width="63%">
Adds an object to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/certenroll/nf-certenroll-ipolicyqualifiers-clear">Clear</a>
</td>
<td align="left" width="63%">
Removes all objects from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/certenroll/nf-certenroll-ipolicyqualifiers-remove">Remove</a>
</td>
<td align="left" width="63%">
Removes an object from the collection by index value.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPolicyQualifiers</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/certenroll/nf-certenroll-ipolicyqualifiers-get__newenum">_NewEnum</a>


</td>
<td align="left" width="63%">
Retrieves the enumerator for the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/certenroll/nf-certenroll-ipolicyqualifiers-get_count">Count</a>


</td>
<td align="left" width="63%">
Retrieves the number of objects in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/certenroll/nf-certenroll-ipolicyqualifiers-get_itembyindex">ItemByIndex</a>


</td>
<td align="left" width="63%">
Retrieves an object from the collection by index number.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ipolicyqualifier">IPolicyQualifier</a>