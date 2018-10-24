---
UID: NN:faxcom.IFaxDoc
title: IFaxDoc
author: windows-sdk-content
description: The IFaxDoc dual interface is used by a fax client application to transmit fax documents and cover pages.
old-location: fax\_mfax_ifaxdoc.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_6mub.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: IFaxDoc, IFaxDoc interface [Fax Service], IFaxDoc interface [Fax Service],described, _mfax_ifaxdoc, fax._mfax_ifaxdoc, faxcom/IFaxDoc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: faxcom.h
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
req.dll: Faxcom.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Faxcom.dll
api_name:
 - IFaxDoc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxDoc interface


## -description


The <b>IFaxDoc</b> dual interface is used by a fax client application to transmit fax documents and cover pages. The interface retrieves and sets information about <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> objects. Information includes the name of the file to transmit, the fax number to which the fax server should send the fax, cover page settings, and other optional fax recipient and sender information.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxDoc</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IFaxDoc</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFaxDoc</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms692792(v=VS.85).aspx">IFaxDoc::Send</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms692792(v=VS.85).aspx">Send</a> method transmits the document specified by the <a href="https://msdn.microsoft.com/en-us/library/ms692340(v=VS.85).aspx">FileName</a> property of a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The method can send the fax to the fax number specified by the <a href="https://msdn.microsoft.com/en-us/library/ms692360(v=VS.85).aspx">FaxNumber</a> property.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxDoc</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms692809(v=VS.85).aspx">IFaxDoc::get_BillingCode</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms692809(v=VS.85).aspx">BillingCode</a> property of a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>BillingCode</b> property is a null-terminated string that contains an optional billing code that applies to the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms692804(v=VS.85).aspx">IFaxDoc::get_CallHandle</a>


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

<a href="https://msdn.microsoft.com/en-us/library/ms691453(v=VS.85).aspx">IFaxDoc::get_CoverpageName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms691453(v=VS.85).aspx">CoverpageName</a> property for a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>CoverpageName</b> property is a null-terminated string that contains the name of the cover page template file (.cov) associated with the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms691857(v=VS.85).aspx">IFaxDoc::get_CoverpageNote</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms691857(v=VS.85).aspx">CoverpageNote</a> property of a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>CoverpageNote</b> property is a null-terminated string that contains the text of a message or note from the sender that pertains to the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms692292(v=VS.85).aspx">IFaxDoc::get_CoverpageSubject</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms692292(v=VS.85).aspx">CoverpageSubject</a> property of a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>CoverpageSubject</b> property is a null-terminated string that contains the subject line of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms691359(v=VS.85).aspx">IFaxDoc::get_DiscountSend</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms691359(v=VS.85).aspx">DiscountSend</a> property for a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>DiscountSend</b> property is a Boolean value that indicates whether the fax server transmits faxes during the discount period.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms691852(v=VS.85).aspx">IFaxDoc::get_DisplayName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms691852(v=VS.85).aspx">DisplayName</a> property of a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>DisplayName</b> property is a null-terminated string that contains the name to associate with the fax document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms692336(v=VS.85).aspx">IFaxDoc::get_EmailAddress</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms692336(v=VS.85).aspx">EmailAddress</a> property of a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>EmailAddress</b> property is a null-terminated string that contains the email address of the sender of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms692360(v=VS.85).aspx">IFaxDoc::get_FaxNumber</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms692360(v=VS.85).aspx">FaxNumber</a> property of a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>FaxNumber</b> property is a null-terminated string that contains the fax number to which the fax server will send the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms692340(v=VS.85).aspx">IFaxDoc::get_FileName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms692340(v=VS.85).aspx">FileName</a> property for a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>FileName</b> property is a null-terminated string that contains the name of the document file associated with the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms692362(v=VS.85).aspx">IFaxDoc::get_RecipientAddress</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms692362(v=VS.85).aspx">RecipientAddress</a> property of a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>RecipientAddress</b> property is a null-terminated string that contains the street address of the recipient of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms691865(v=VS.85).aspx">IFaxDoc::get_RecipientCity</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms691865(v=VS.85).aspx">RecipientCity</a> property of a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>RecipientCity</b> property is a null-terminated string that contains the city name of the recipient of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms690860(v=VS.85).aspx">IFaxDoc::get_RecipientCompany</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms690860(v=VS.85).aspx">RecipientCompany</a> property of a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>RecipientCompany</b> property is a null-terminated string that contains the company name of the recipient of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms692357(v=VS.85).aspx">IFaxDoc::get_RecipientCountry</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms692357(v=VS.85).aspx">RecipientCountry</a> property of a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>RecipientCountry</b> property is a null-terminated string that contains the country/region of the recipient of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms691468(v=VS.85).aspx">IFaxDoc::get_RecipientDepartment</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms691468(v=VS.85).aspx">RecipientDepartment</a> property of a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>RecipientDepartment</b> property is a null-terminated string that contains the department of the recipient of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms692830(v=VS.85).aspx">IFaxDoc::get_RecipientHomePhone</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms692830(v=VS.85).aspx">RecipientHomePhone</a> property of a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>RecipientHomePhone</b> property is a null-terminated string that contains the home telephone number of the recipient of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms691938(v=VS.85).aspx">IFaxDoc::get_RecipientName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms691938(v=VS.85).aspx">RecipientName</a> property of a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>RecipientName</b> property is a null-terminated string that contains the name of the recipient of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms691885(v=VS.85).aspx">IFaxDoc::get_RecipientOffice</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms691885(v=VS.85).aspx">RecipientOffice</a> property of a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>RecipientOffice</b> property is a null-terminated string that contains the office of the recipient of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms691390(v=VS.85).aspx">IFaxDoc::get_RecipientOfficePhone</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms691390(v=VS.85).aspx">RecipientOfficePhone</a> property of a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>RecipientOfficePhone</b> property is a null-terminated string that contains the office telephone number of the recipient of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms691495(v=VS.85).aspx">IFaxDoc::get_RecipientState</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms691495(v=VS.85).aspx">RecipientState</a> property of a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>RecipientState</b> property is a null-terminated string that contains the state of the recipient of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms691408(v=VS.85).aspx">IFaxDoc::get_RecipientTitle</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms691408(v=VS.85).aspx">RecipientTitle</a> property of a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>RecipientTitle</b> property is a null-terminated string that contains the title of the recipient of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms691350(v=VS.85).aspx">IFaxDoc::get_RecipientZip</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms691350(v=VS.85).aspx">RecipientZip</a> property of a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>RecipientZip</b> property is a null-terminated string that contains the ZIP code of the recipient of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms690916(v=VS.85).aspx">IFaxDoc::get_SendCoverpage</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms690916(v=VS.85).aspx">SendCoverpage</a> property for a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>SendCoverpage</b> property is a Boolean value that indicates whether the specified cover page file is stored on the fax server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms691893(v=VS.85).aspx">IFaxDoc::get_SenderAddress</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms691893(v=VS.85).aspx">SenderAddress</a> property of a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>SenderAddress</b> property is a null-terminated string that contains the street address of the sender of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms692355(v=VS.85).aspx">IFaxDoc::get_SenderCompany</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms692355(v=VS.85).aspx">SenderCompany</a> property of a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>SenderCompany</b> property is a null-terminated string that contains the company name of the sender of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms690835(v=VS.85).aspx">IFaxDoc::get_SenderDepartment</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms690835(v=VS.85).aspx">SenderDepartment</a> property of a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>SenderDepartment</b> property is a null-terminated string that contains the department of the sender of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms690712(v=VS.85).aspx">IFaxDoc::get_SenderFax</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms690712(v=VS.85).aspx">SenderFax</a> property of a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>SenderFax</b> property is a null-terminated string that contains the fax number of the sender of the outbound fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms692800(v=VS.85).aspx">IFaxDoc::get_SenderHomePhone</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms692800(v=VS.85).aspx">SenderHomePhone</a> property of a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>SenderHomePhone</b> property is a null-terminated string that contains the home telephone number of the sender of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms692811(v=VS.85).aspx">IFaxDoc::get_SenderName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms692811(v=VS.85).aspx">SenderName</a> property of a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>SenderName</b> property is a null-terminated string that contains the name of the sender of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms692327(v=VS.85).aspx">IFaxDoc::get_SenderOffice</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms692327(v=VS.85).aspx">SenderOffice</a> property of a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>SenderOffice</b> property is a null-terminated string that contains the office of the sender of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms690842(v=VS.85).aspx">IFaxDoc::get_SenderOfficePhone</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms690842(v=VS.85).aspx">SenderOfficePhone</a> property of a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>SenderOfficePhone</b> property is a null-terminated string that contains the office telephone number of the sender of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms691474(v=VS.85).aspx">IFaxDoc::get_SenderTitle</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms691474(v=VS.85).aspx">SenderTitle</a> property of a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>SenderTitle</b> property is a null-terminated string that contains the title of the sender of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms690883(v=VS.85).aspx">IFaxDoc::get_ServerCoverpage</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms690883(v=VS.85).aspx">ServerCoverpage</a> property for a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>ServerCoverpage</b> property is a Boolean value that indicates whether the specified cover page file is stored on the fax server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms691503(v=VS.85).aspx">IFaxDoc::get_Tsid</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms691503(v=VS.85).aspx">Tsid</a> property of a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>Tsid</b> property is a null-terminated string that contains a user-defined TSID.

</td>
</tr>
</table> 


## -remarks



The <b>IFaxDoc</b> interface includes the following methods:

<ul>
<li>A method to send a fax document.</li>
<li>Property methods to set and retrieve individual property values associated with a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object.</li>
</ul>
<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
You should not implement this interface. The Microsoft standard implementation provides complete functionality.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Use the <b>IFaxDoc</b> interface to send a fax document. You can also use the <b>IFaxDoc</b> interface to retrieve and set the properties of a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object.

A client application should not call the <a href="https://msdn.microsoft.com/en-us/library/ms686615(v=VS.85).aspx">CoCreateInstance</a> function to retrieve an <b>IFaxDoc</b> interface pointer. Instead, the application must perform the following steps to create an instance of a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object: 
                

<ol>
<li>Call the <a href="https://msdn.microsoft.com/en-us/library/ms686615(v=VS.85).aspx">CoCreateInstance</a> function to retrieve a pointer to an <a href="https://msdn.microsoft.com/en-us/library/ms692375(v=VS.85).aspx">IFaxServer</a> interface.</li>
<li>Call the <a href="https://msdn.microsoft.com/en-us/library/ms692315(v=VS.85).aspx">IFaxServer::Connect</a> method to connect to an active fax server. </li>
<li>Call the <a href="https://msdn.microsoft.com/en-us/library/ms690786(v=VS.85).aspx">IFaxServer::CreateDocument</a> method to create and initialize a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object for the connected fax server. (After calling the <b>IFaxServer::CreateDocument</b> method, you can also call the <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">IUnknown::QueryInterface</a> method to retrieve an <b>IFaxDoc</b> interface pointer.)</li>
<li>Use the <b>IDispatch</b> interface pointer to call <b>IFaxDoc</b> interface methods.</li>
<li>Call the <a href="https://msdn.microsoft.com/en-us/library/ms691936(v=VS.85).aspx">IFaxServer::Disconnect</a> method to disconnect from the fax server.</li>
<li>Call the <a href="https://msdn.microsoft.com/en-us/library/ms682317(v=VS.85).aspx">IUnknown::Release</a> method to destroy the <b>IFaxDoc</b> interface pointer, and the parent <a href="https://msdn.microsoft.com/en-us/library/ms692375(v=VS.85).aspx">IFaxServer</a> interface pointer.</li>
</ol>
The property methods of the <b>IFaxDoc</b> interface get or set the properties described following. If the property supports read access, the <b>IFaxDoc</b> interface includes a <i>get_PropertyName</i> method. If the property supports write access, the interface includes a <i>put_PropertyName</i> method.

Values are not required for optional properties that appear only on the cover page. The <a href="https://msdn.microsoft.com/en-us/library/ms692340(v=VS.85).aspx">FileName</a> property is required to send a fax transmission using a call to the <a href="https://msdn.microsoft.com/en-us/library/ms692792(v=VS.85).aspx">IFaxDoc::Send</a> method. The <a href="https://msdn.microsoft.com/en-us/library/ms692360(v=VS.85).aspx">FaxNumber</a> property is also required.

The fax server can supply data from the registry for many properties that begin with <b>Sender</b>. The fax server supplies values if they have been entered under the <b>User Information</b> tab accessed through the Fax icon in Control Panel.

Following are the properties associated with a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>
 

 

