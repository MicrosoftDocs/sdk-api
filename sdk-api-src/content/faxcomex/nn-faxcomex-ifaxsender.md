---
UID: NN:faxcomex.IFaxSender
title: IFaxSender
author: windows-sdk-content
description: The IFaxSender interface defines a messaging object used by a fax client application to retrieve and set sender information about fax senders. The object also includes methods to store sender data in and retrieve sender data from the local registry.
old-location: fax\_mfax_faxsender_cpp.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_0gtu_cpp.htm
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IFaxSender, IFaxSender interface [Fax Service], IFaxSender interface [Fax Service],described, _mfax_faxsender_cpp, fax._mfax_faxsender_cpp, faxcomex/IFaxSender
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
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
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxSender interface


## -description


The <b>IFaxSender</b> interface defines a messaging object used by a fax client application to retrieve and set sender information about fax senders. The object also includes methods to store sender data in and retrieve sender data from the local registry.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxSender</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFaxSender</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/c41343c0-2d97-4bc5-ba22-a7dfec5cb336">LoadDefaultSender</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/c41343c0-2d97-4bc5-ba22-a7dfec5cb336">IFaxSender::get_LoadDefaultSender</a> method fills the <a href="https://msdn.microsoft.com/f265cfd0-cf62-4d86-9ba5-d1842ac94baa">FaxSender</a> object with the default sender information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c06c0a8e-6016-40e8-864e-cfeae8c5994e">SaveDefaultSender</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/c06c0a8e-6016-40e8-864e-cfeae8c5994e">IFaxSender::SaveDefaultSender</a> method stores information about the default sender from the <a href="https://msdn.microsoft.com/f265cfd0-cf62-4d86-9ba5-d1842ac94baa">FaxSender</a> object.

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

<a href="https://msdn.microsoft.com/75427436-868c-411f-a804-d70e6e19358f">BillingCode</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/75427436-868c-411f-a804-d70e6e19358f">IFaxSender::get_BillingCode</a> property is a null-terminated string that contains the billing code associated with the sender.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e7aad4a2-410e-4f94-92f8-38fc34c35bd2">City</a>


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

<a href="https://msdn.microsoft.com/53baa4ef-f6e3-4996-9f28-fdb1542b1a30">Company</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/53baa4ef-f6e3-4996-9f28-fdb1542b1a30">IFaxSender::get_Company</a> property is a null-terminated string that contains the company name associated with the sender.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/747cd438-1df3-4fbf-9867-1ae669e6a660">Country</a>


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

<a href="https://msdn.microsoft.com/35271821-369d-4b7d-80fa-19659f9d318e">Department</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/35271821-369d-4b7d-80fa-19659f9d318e">IFaxSender::get_Department</a> property is a null-terminated string that contains the department associated with the sender.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/mt168420">Email</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/292562dd-9364-4e67-b0a6-7026867a34d0">IFaxSender::get_Email</a> property is a null-terminated string that contains the email address associated with the sender.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e5528757-06d0-4879-a873-1682b18d69c1">FaxNumber</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/e5528757-06d0-4879-a873-1682b18d69c1">IFaxSender::get_FaxNumber</a> property is a null-terminated string that contains the fax number associated with the sender.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/2a6d9fb3-0eef-488e-aefd-ac03735c5771">HomePhone</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/2a6d9fb3-0eef-488e-aefd-ac03735c5771">IFaxSender::get_HomePhone</a> property is a null-terminated string that contains the home telephone number associated with the sender.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/ad01dcca-ad01-4aea-80fa-2655ad38015b">IFaxSender::get_Name</a> property is a null-terminated string that contains the name of the sender.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/448c5867-6249-4aab-8efb-1586064d17d0">OfficeLocation</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/448c5867-6249-4aab-8efb-1586064d17d0">IFaxSender::get_OfficeLocation</a> property is a null-terminated string that contains the office location of the sender.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/77512e8d-d0a5-44f0-8320-a1ab17436e3c">OfficePhone</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/77512e8d-d0a5-44f0-8320-a1ab17436e3c">IFaxSender::get_OfficePhone</a> property is a null-terminated string that contains the office telephone number associated with the sender.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/da9fff74-790a-4563-a574-ef4f4003f2fb">State</a>


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

<a href="https://msdn.microsoft.com/a0c4fd70-105b-4560-a18e-6e51849f1901">StreetAddress</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/a0c4fd70-105b-4560-a18e-6e51849f1901">IFaxSender::get_StreetAddress</a> property is a null-terminated string that contains the street address associated with the sender.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn923257">Title</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/46303355-f186-4b5c-80fc-d106b7d7df34">IFaxSender::get_Title</a> property is a null-terminated string that contains the title associated with the sender.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn997387">TSID</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/50d42e18-b79c-4356-9222-de506c6105d1">IFaxSender::get_TSID</a> property is a null-terminated string that contains the transmitting station identifier (TSID) for the sender's device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9815c8a9-27c4-4df2-94c0-d51ef463afda">ZipCode</a>


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



A default implementation of <b>IFaxSender</b> is provided as the <a href="https://msdn.microsoft.com/f265cfd0-cf62-4d86-9ba5-d1842ac94baa">FaxSender</a> object.



