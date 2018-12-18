---
UID: NN:faxcomex.IFaxSender
title: IFaxSender
author: windows-sdk-content
description: The IFaxSender interface defines a messaging object used by a fax client application to retrieve and set sender information about fax senders. The object also includes methods to store sender data in and retrieve sender data from the local registry.
old-location: fax\_mfax_faxsender_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_0gtu_cpp.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxSender, IFaxSender interface [Fax Service], IFaxSender interface [Fax Service],described, _mfax_faxsender_cpp, fax._mfax_faxsender_cpp, faxcomex/IFaxSender
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
---

# IFaxSender interface


## -description


The <b>IFaxSender</b> interface defines a messaging object used by a fax client application to retrieve and set sender information about fax senders. The object also includes methods to store sender data in and retrieve sender data from the local registry.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxSender</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IFaxSender</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/ms690195(v=VS.85).aspx">LoadDefaultSender</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms690195(v=VS.85).aspx">IFaxSender::get_LoadDefaultSender</a> method fills the <a href="https://msdn.microsoft.com/en-us/library/ms687532(v=VS.85).aspx">FaxSender</a> object with the default sender information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms689558(v=VS.85).aspx">SaveDefaultSender</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms689558(v=VS.85).aspx">IFaxSender::SaveDefaultSender</a> method stores information about the default sender from the <a href="https://msdn.microsoft.com/en-us/library/ms687532(v=VS.85).aspx">FaxSender</a> object.

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

<a href="https://msdn.microsoft.com/en-us/library/ms689541(v=VS.85).aspx">BillingCode</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms689541(v=VS.85).aspx">IFaxSender::get_BillingCode</a> property is a null-terminated string that contains the billing code associated with the sender.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms689516(v=VS.85).aspx">City</a>


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

<a href="https://msdn.microsoft.com/en-us/library/ms688437(v=VS.85).aspx">Company</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms688437(v=VS.85).aspx">IFaxSender::get_Company</a> property is a null-terminated string that contains the company name associated with the sender.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms690217(v=VS.85).aspx">Country</a>


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

<a href="https://msdn.microsoft.com/en-us/library/ms689597(v=VS.85).aspx">Department</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms689597(v=VS.85).aspx">IFaxSender::get_Department</a> property is a null-terminated string that contains the department associated with the sender.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms688301(v=VS.85).aspx">Email</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms688301(v=VS.85).aspx">IFaxSender::get_Email</a> property is a null-terminated string that contains the email address associated with the sender.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms687520(v=VS.85).aspx">FaxNumber</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms687520(v=VS.85).aspx">IFaxSender::get_FaxNumber</a> property is a null-terminated string that contains the fax number associated with the sender.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms690265(v=VS.85).aspx">HomePhone</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms690265(v=VS.85).aspx">IFaxSender::get_HomePhone</a> property is a null-terminated string that contains the home telephone number associated with the sender.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms689577(v=VS.85).aspx">Name</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms689577(v=VS.85).aspx">IFaxSender::get_Name</a> property is a null-terminated string that contains the name of the sender.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms687522(v=VS.85).aspx">OfficeLocation</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms687522(v=VS.85).aspx">IFaxSender::get_OfficeLocation</a> property is a null-terminated string that contains the office location of the sender.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms687969(v=VS.85).aspx">OfficePhone</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms687969(v=VS.85).aspx">IFaxSender::get_OfficePhone</a> property is a null-terminated string that contains the office telephone number associated with the sender.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms689194(v=VS.85).aspx">State</a>


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

<a href="https://msdn.microsoft.com/en-us/library/ms690078(v=VS.85).aspx">StreetAddress</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms690078(v=VS.85).aspx">IFaxSender::get_StreetAddress</a> property is a null-terminated string that contains the street address associated with the sender.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms689144(v=VS.85).aspx">Title</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms689144(v=VS.85).aspx">IFaxSender::get_Title</a> property is a null-terminated string that contains the title associated with the sender.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms688471(v=VS.85).aspx">TSID</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms688471(v=VS.85).aspx">IFaxSender::get_TSID</a> property is a null-terminated string that contains the transmitting station identifier (TSID) for the sender's device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms688617(v=VS.85).aspx">ZipCode</a>


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



A default implementation of <b>IFaxSender</b> is provided as the <a href="https://msdn.microsoft.com/en-us/library/ms687532(v=VS.85).aspx">FaxSender</a> object.



