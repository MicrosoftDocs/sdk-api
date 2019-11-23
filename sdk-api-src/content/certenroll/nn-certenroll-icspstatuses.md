---
UID: NN:certenroll.ICspStatuses
title: ICspStatuses (certenroll.h)

description: Contains information about a cryptographic provider/algorithm pair.
old-location: security\icspstatuses.htm
tech.root: seccertenroll
ms.assetid: 73d0f3a7-7afd-42c9-88db-911531c50137

ms.date: 12/05/2018
ms.keywords: ICspStatuses, ICspStatuses interface [Security], ICspStatuses interface [Security],described, certenroll/ICspStatuses, security.icspstatuses
ms.topic: interface
f1_keywords: 
 - "certenroll/ICspStatuses"
dev_langs:
 - c++
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
 - ICspStatuses
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICspStatuses interface


## -description


The <b>ICspStatuses</b> interface defines methods and properties that can be used to manage a collection of <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icspstatus">ICspStatus</a> objects. The <b>ICspStatus</b> interface contains information about a  cryptographic provider/algorithm pair.   The collection object is created when you call the following properties and methods.<table>
<tr>
<th>Property/Method</th>
<th>Interface</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspinformations-getcspstatusesfromoperations">GetCspStatusesFromOperations</a>
</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icspinformations">ICspInformations</a>
</td>
<td>Creates an <b>ICspStatuses</b> collection for a specified algorithm type and optional provider information.<div class="alert"><b>Note</b>  The Certificate Enrollment Control uses an <b>ICspStatuses</b> collection only for private key asymmetric (encryption, signing, and key exchange) algorithm  selection.</div>
<div> </div>
</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-getcspstatuses">GetCspStatuses</a>
</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a>
</td>
<td>Creates an <b>ICspStatuses</b> collection that contains all  provider/algorithm pairs consistent with the intended use of the private key as specified by the caller.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-get_cspstatuses">CspStatuses</a>
</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a>
</td>
<td>Creates an <b>ICspStatuses</b> collection that contains all  provider/algorithm pairs consistent with the intended use of the private key as identified by the IX509PrivateKey object associated with the certificate request.</td>
</tr>
</table>
 




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICspStatuses</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ICspStatuses</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ICspStatuses</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspstatuses-add">Add</a>
</td>
<td align="left" width="63%">
Adds an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icspstatus">ICspStatus</a> object to the collection.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspstatuses-clear">Clear</a>
</td>
<td align="left" width="63%">
Removes all <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icspstatus">ICspStatus</a> objects from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspstatuses-remove">Remove</a>
</td>
<td align="left" width="63%">
Removes an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icspstatus">ICspStatus</a> object from the collection by index number.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICspStatuses</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspstatuses-get__newenum">_NewEnum</a>


</td>
<td align="left" width="63%">
Retrieves the enumerator for the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspstatuses-get_count">Count</a>


</td>
<td align="left" width="63%">
Retrieves the number of <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icspstatus">ICspStatus</a> objects in the collection.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspstatuses-get_itembyindex">ItemByIndex</a>


</td>
<td align="left" width="63%">
Retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icspstatus">ICspStatus</a> object from the collection by index number.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspstatuses-get_itembyname">ItemByName</a>


</td>
<td align="left" width="63%">
Retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icspstatus">ICspStatus</a> object from the collection by provider and algorithm name.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspstatuses-get_itembyoperations">ItemByOperations</a>


</td>
<td align="left" width="63%">
Retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icspstatus">ICspStatus</a> object that has the same name as the  provider specified on input and the same algorithm but identifies a different cryptographic operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspstatuses-get_itembyordinal">ItemByOrdinal</a>


</td>
<td align="left" width="63%">
Retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icspstatus">ICspStatus</a> object from the collection by ordinal number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspstatuses-get_itembyprovider">ItemByProvider</a>


</td>
<td align="left" width="63%">
Retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icspstatus">ICspStatus</a> object that has the same name as the  provider specified on input but identifies an algorithm that supports a different intended key use.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icspstatus">ICspStatus</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
 

 

