---
UID: NN:certenroll.ISignerCertificates
title: ISignerCertificates (certenroll.h)
author: windows-sdk-content
description: The ISignerCertificates interface defines the following methods and properties to manage a collection of ISignerCertificate objects.
old-location: security\isignercertificates.htm
tech.root: seccertenroll
ms.assetid: 420d6550-514a-4fea-987b-6deecbc9b717
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISignerCertificates, ISignerCertificates interface [Security], ISignerCertificates interface [Security],described, certenroll/ISignerCertificates, security.isignercertificates
ms.topic: interface
f1_keywords: ["certenroll/ISignerCertificates"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - ISignerCertificates
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISignerCertificates interface


## -description


The <b>ISignerCertificates</b> interface defines the following methods and properties to manage a collection of <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-isignercertificate">ISignerCertificate</a> objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISignerCertificates</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ISignerCertificates</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ISignerCertificates</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-isignercertificates-add">Add</a>
</td>
<td align="left" width="63%">
Adds an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-isignercertificate">ISignerCertificate</a> object to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-isignercertificates-clear">Clear</a>
</td>
<td align="left" width="63%">
Removes all <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-isignercertificate">ISignerCertificate</a> objects from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-isignercertificates-find">Find</a>
</td>
<td align="left" width="63%">
Retrieves the index number of an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-isignercertificate">ISignerCertificate</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-isignercertificates-remove">Remove</a>
</td>
<td align="left" width="63%">
Removes an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-isignercertificate">ISignerCertificate</a> object from the collection by index number.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISignerCertificates</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-isignercertificates-get__newenum">_NewEnum</a>


</td>
<td align="left" width="63%">
Retrieves the enumerator for the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-isignercertificates-get_count">Count</a>


</td>
<td align="left" width="63%">
Retrieves the number of <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-isignercertificate">ISignerCertificate</a> objects in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-isignercertificates-get_itembyindex">ItemByIndex</a>


</td>
<td align="left" width="63%">
Retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-isignercertificate">ISignerCertificate</a> object from the collection by index number.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/certificate-enrollment-api-reference">Certificate Enrollment API</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-isignercertificate">ISignerCertificate</a>
 

 

