---
UID: NN:certenroll.ICspInformations
title: ICspInformations (certenroll.h)
author: windows-sdk-content
description: The ICspInformations interface defines the following methods and properties to manage a collection of ICspInformation objects.
old-location: security\icspinformations.htm
tech.root: seccertenroll
ms.assetid: 8141023c-c162-46d6-9c37-e227ce1c8761
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICspInformations, ICspInformations interface [Security], ICspInformations interface [Security],described, certenroll/ICspInformations, security.icspinformations
ms.topic: interface
f1_keywords: 
 - "certenroll/ICspInformations"
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
 - ICspInformations
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICspInformations interface


## -description


The <b>ICspInformations</b> interface defines the following methods and properties to manage a collection of <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a> objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICspInformations</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ICspInformations</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ICspInformations</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspinformations-add">Add</a>
</td>
<td align="left" width="63%">
Adds an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a> object to the collection.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspinformations-addavailablecsps">AddAvailableCsps</a>
</td>
<td align="left" width="63%">
Adds the providers installed on the computer to the collection.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspinformations-clear">Clear</a>
</td>
<td align="left" width="63%">
Removes all <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a> objects from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspinformations-getcspstatusesfromoperations">GetCspStatusesFromOperations</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icspstatuses">ICspStatuses</a> collection by supported key operations and optional provider information.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspinformations-getcspstatusfromprovidername">GetCspStatusFromProviderName</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icspstatus">ICspStatus</a> object for a legacy provider by provider name and supported key operations.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspinformations-getencryptioncspalgorithms">GetEncryptionCspAlgorithms</a>
</td>
<td align="left" width="63%">
Retrieves the  collection of encryption algorithms supported by a provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspinformations-gethashalgorithms">GetHashAlgorithms</a>
</td>
<td align="left" width="63%">
Retrieves the collection of hash algorithms supported by a provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspinformations-remove">Remove</a>
</td>
<td align="left" width="63%">
Removes an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a> object from the collection by index number.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICspInformations</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspinformations-get__newenum">_NewEnum</a>


</td>
<td align="left" width="63%">
Retrieves the enumerator for the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspinformations-get_count">Count</a>


</td>
<td align="left" width="63%">
Retrieves the number of <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a> objects in the collection.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspinformations-get_itembyindex">ItemByIndex</a>


</td>
<td align="left" width="63%">
Retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a> object from the collection by index number.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspinformations-get_itembyname">ItemByName</a>


</td>
<td align="left" width="63%">
Retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a> object from the collection by name.

[WebEnabled]

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
 

 

