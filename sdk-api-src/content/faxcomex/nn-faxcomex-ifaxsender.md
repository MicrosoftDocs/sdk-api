---
UID: NN:faxcomex.IFaxSender
title: IFaxSender (faxcomex.h)
author: windows-sdk-content
description: The IFaxSender interface defines a messaging object used by a fax client application to retrieve and set sender information about fax senders. The object also includes methods to store sender data in and retrieve sender data from the local registry.
old-location: fax\_mfax_faxsender_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_0gtu_cpp.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFaxSender, IFaxSender interface [Fax Service], IFaxSender interface [Fax Service],described, _mfax_faxsender_cpp, fax._mfax_faxsender_cpp, faxcomex/IFaxSender
ms.topic: interface
f1_keywords: 
 - "faxcomex/IFaxSender"
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Fxscomex.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxSender
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxSender interface


## -description


The <b>IFaxSender</b> interface defines a messaging object used by a fax client application to retrieve and set sender information about fax senders. The object also includes methods to store sender data in and retrieve sender data from the local registry.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxSender</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxSender</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFaxSender</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxsender-loaddefaultsender-vb">LoadDefaultSender</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxsender-loaddefaultsender-vb">IFaxSender::get_LoadDefaultSender</a> method fills the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxsender">FaxSender</a> object with the default sender information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxsender-savedefaultsender-vb">SaveDefaultSender</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxsender-savedefaultsender-vb">IFaxSender::SaveDefaultSender</a> method stores information about the default sender from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxsender">FaxSender</a> object.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxSender</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxsender-billingcode-vb">BillingCode</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxsender-billingcode-vb">IFaxSender::get_BillingCode</a> property is a null-terminated string that contains the billing code associated with the sender.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxsender-city-vb">City</a>


</td>
<td align="left" width="10%">
Write-only

</td>
<td align="left" width="63%">
Not currently supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxsender-company-vb">Company</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxsender-company-vb">IFaxSender::get_Company</a> property is a null-terminated string that contains the company name associated with the sender.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxsender-country-vb">Country</a>


</td>
<td align="left" width="10%">
Write-only

</td>
<td align="left" width="63%">
Not currently supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxsender-department-vb">Department</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxsender-department-vb">IFaxSender::get_Department</a> property is a null-terminated string that contains the department associated with the sender.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxsender-email-vb">Email</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxsender-email-vb">IFaxSender::get_Email</a> property is a null-terminated string that contains the email address associated with the sender.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxsender-faxnumber-vb">FaxNumber</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxsender-faxnumber-vb">IFaxSender::get_FaxNumber</a> property is a null-terminated string that contains the fax number associated with the sender.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxsender-homephone-vb">HomePhone</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxsender-homephone-vb">IFaxSender::get_HomePhone</a> property is a null-terminated string that contains the home telephone number associated with the sender.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxsender-name-vb">Name</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxsender-name-vb">IFaxSender::get_Name</a> property is a null-terminated string that contains the name of the sender.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxsender-officelocation-vb">OfficeLocation</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxsender-officelocation-vb">IFaxSender::get_OfficeLocation</a> property is a null-terminated string that contains the office location of the sender.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxsender-officephone-vb">OfficePhone</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxsender-officephone-vb">IFaxSender::get_OfficePhone</a> property is a null-terminated string that contains the office telephone number associated with the sender.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxsender-state-vb">State</a>


</td>
<td align="left" width="10%">
Write-only

</td>
<td align="left" width="63%">
Not currently supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxsender-streetaddress-vb">StreetAddress</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxsender-streetaddress-vb">IFaxSender::get_StreetAddress</a> property is a null-terminated string that contains the street address associated with the sender.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxsender-title-vb">Title</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxsender-title-vb">IFaxSender::get_Title</a> property is a null-terminated string that contains the title associated with the sender.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxsender-tsid-vb">TSID</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxsender-tsid-vb">IFaxSender::get_TSID</a> property is a null-terminated string that contains the transmitting station identifier (TSID) for the sender's device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxsender-zipcode-vb">ZipCode</a>


</td>
<td align="left" width="10%">
Write-only

</td>
<td align="left" width="63%">
Not currently supported.

</td>
</tr>
</table> 


## -remarks



A default implementation of <b>IFaxSender</b> is provided as the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxsender">FaxSender</a> object.



