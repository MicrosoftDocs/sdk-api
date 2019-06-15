---
UID: NN:faxcom.IFaxDoc
title: IFaxDoc (faxcom.h)
author: windows-sdk-content
description: The IFaxDoc dual interface is used by a fax client application to transmit fax documents and cover pages.
old-location: fax\_mfax_ifaxdoc.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_6mub.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFaxDoc, IFaxDoc interface [Fax Service], IFaxDoc interface [Fax Service],described, _mfax_ifaxdoc, fax._mfax_ifaxdoc, faxcom/IFaxDoc
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
ms.custom: 19H1
---

# IFaxDoc interface


## -description


The <b>IFaxDoc</b> dual interface is used by a fax client application to transmit fax documents and cover pages. The interface retrieves and sets information about <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> objects. Information includes the name of the file to transmit, the fax number to which the fax server should send the fax, cover page settings, and other optional fax recipient and sender information.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxDoc</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxDoc</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-send-vb">IFaxDoc::Send</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-send-vb">Send</a> method transmits the document specified by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-filename-vb">FileName</a> property of a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The method can send the fax to the fax number specified by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-faxnumber-vb">FaxNumber</a> property.

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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-billingcode-vb">IFaxDoc::get_BillingCode</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-billingcode-vb">BillingCode</a> property of a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>BillingCode</b> property is a null-terminated string that contains an optional billing code that applies to the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-callhandle-vb">IFaxDoc::get_CallHandle</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-coverpagename-vb">IFaxDoc::get_CoverpageName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-coverpagename-vb">CoverpageName</a> property for a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>CoverpageName</b> property is a null-terminated string that contains the name of the cover page template file (.cov) associated with the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-coverpagenote-vb">IFaxDoc::get_CoverpageNote</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-coverpagenote-vb">CoverpageNote</a> property of a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>CoverpageNote</b> property is a null-terminated string that contains the text of a message or note from the sender that pertains to the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-coverpagesubject-vb">IFaxDoc::get_CoverpageSubject</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-coverpagesubject-vb">CoverpageSubject</a> property of a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>CoverpageSubject</b> property is a null-terminated string that contains the subject line of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-discountsend-vb">IFaxDoc::get_DiscountSend</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-discountsend-vb">DiscountSend</a> property for a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>DiscountSend</b> property is a Boolean value that indicates whether the fax server transmits faxes during the discount period.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-displayname-vb">IFaxDoc::get_DisplayName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-displayname-vb">DisplayName</a> property of a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>DisplayName</b> property is a null-terminated string that contains the name to associate with the fax document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-emailaddress-vb">IFaxDoc::get_EmailAddress</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-emailaddress-vb">EmailAddress</a> property of a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>EmailAddress</b> property is a null-terminated string that contains the email address of the sender of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-faxnumber-vb">IFaxDoc::get_FaxNumber</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-faxnumber-vb">FaxNumber</a> property of a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>FaxNumber</b> property is a null-terminated string that contains the fax number to which the fax server will send the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-filename-vb">IFaxDoc::get_FileName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-filename-vb">FileName</a> property for a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>FileName</b> property is a null-terminated string that contains the name of the document file associated with the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-recipientaddress-vb">IFaxDoc::get_RecipientAddress</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-recipientaddress-vb">RecipientAddress</a> property of a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>RecipientAddress</b> property is a null-terminated string that contains the street address of the recipient of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-recipientcity-vb">IFaxDoc::get_RecipientCity</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-recipientcity-vb">RecipientCity</a> property of a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>RecipientCity</b> property is a null-terminated string that contains the city name of the recipient of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-recipientcompany-vb">IFaxDoc::get_RecipientCompany</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-recipientcompany-vb">RecipientCompany</a> property of a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>RecipientCompany</b> property is a null-terminated string that contains the company name of the recipient of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-recipientcountry-vb">IFaxDoc::get_RecipientCountry</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-recipientcountry-vb">RecipientCountry</a> property of a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>RecipientCountry</b> property is a null-terminated string that contains the country/region of the recipient of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-recipientdepartment-vb">IFaxDoc::get_RecipientDepartment</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-recipientdepartment-vb">RecipientDepartment</a> property of a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>RecipientDepartment</b> property is a null-terminated string that contains the department of the recipient of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-recipienthomephone-vb">IFaxDoc::get_RecipientHomePhone</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-recipienthomephone-vb">RecipientHomePhone</a> property of a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>RecipientHomePhone</b> property is a null-terminated string that contains the home telephone number of the recipient of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-recipientname-vb">IFaxDoc::get_RecipientName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-recipientname-vb">RecipientName</a> property of a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>RecipientName</b> property is a null-terminated string that contains the name of the recipient of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-recipientoffice-vb">IFaxDoc::get_RecipientOffice</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-recipientoffice-vb">RecipientOffice</a> property of a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>RecipientOffice</b> property is a null-terminated string that contains the office of the recipient of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-recipientofficephone-vb">IFaxDoc::get_RecipientOfficePhone</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-recipientofficephone-vb">RecipientOfficePhone</a> property of a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>RecipientOfficePhone</b> property is a null-terminated string that contains the office telephone number of the recipient of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-recipientstate-vb">IFaxDoc::get_RecipientState</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-recipientstate-vb">RecipientState</a> property of a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>RecipientState</b> property is a null-terminated string that contains the state of the recipient of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-recipienttitle-vb">IFaxDoc::get_RecipientTitle</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-recipienttitle-vb">RecipientTitle</a> property of a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>RecipientTitle</b> property is a null-terminated string that contains the title of the recipient of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-recipientzip-vb">IFaxDoc::get_RecipientZip</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-recipientzip-vb">RecipientZip</a> property of a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>RecipientZip</b> property is a null-terminated string that contains the ZIP code of the recipient of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-sendcoverpage-vb">IFaxDoc::get_SendCoverpage</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-sendcoverpage-vb">SendCoverpage</a> property for a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>SendCoverpage</b> property is a Boolean value that indicates whether the specified cover page file is stored on the fax server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-senderaddress-vb">IFaxDoc::get_SenderAddress</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-senderaddress-vb">SenderAddress</a> property of a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>SenderAddress</b> property is a null-terminated string that contains the street address of the sender of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-sendercompany-vb">IFaxDoc::get_SenderCompany</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-sendercompany-vb">SenderCompany</a> property of a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>SenderCompany</b> property is a null-terminated string that contains the company name of the sender of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-senderdepartment-vb">IFaxDoc::get_SenderDepartment</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-senderdepartment-vb">SenderDepartment</a> property of a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>SenderDepartment</b> property is a null-terminated string that contains the department of the sender of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-senderfax-vb">IFaxDoc::get_SenderFax</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-senderfax-vb">SenderFax</a> property of a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>SenderFax</b> property is a null-terminated string that contains the fax number of the sender of the outbound fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-senderhomephone-vb">IFaxDoc::get_SenderHomePhone</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-senderhomephone-vb">SenderHomePhone</a> property of a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>SenderHomePhone</b> property is a null-terminated string that contains the home telephone number of the sender of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-sendername-vb">IFaxDoc::get_SenderName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-sendername-vb">SenderName</a> property of a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>SenderName</b> property is a null-terminated string that contains the name of the sender of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-senderoffice-vb">IFaxDoc::get_SenderOffice</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-senderoffice-vb">SenderOffice</a> property of a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>SenderOffice</b> property is a null-terminated string that contains the office of the sender of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-senderofficephone-vb">IFaxDoc::get_SenderOfficePhone</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-senderofficephone-vb">SenderOfficePhone</a> property of a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>SenderOfficePhone</b> property is a null-terminated string that contains the office telephone number of the sender of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-sendertitle-vb">IFaxDoc::get_SenderTitle</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-sendertitle-vb">SenderTitle</a> property of a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>SenderTitle</b> property is a null-terminated string that contains the title of the sender of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-servercoverpage-vb">IFaxDoc::get_ServerCoverpage</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-servercoverpage-vb">ServerCoverpage</a> property for a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>ServerCoverpage</b> property is a Boolean value that indicates whether the specified cover page file is stored on the fax server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-tsid-vb">IFaxDoc::get_Tsid</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-tsid-vb">Tsid</a> property of a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>Tsid</b> property is a null-terminated string that contains a user-defined TSID.

</td>
</tr>
</table> 


## -remarks



The <b>IFaxDoc</b> interface includes the following methods:

<ul>
<li>A method to send a fax document.</li>
<li>Property methods to set and retrieve individual property values associated with a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object.</li>
</ul>
<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
You should not implement this interface. The Microsoft standard implementation provides complete functionality.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Use the <b>IFaxDoc</b> interface to send a fax document. You can also use the <b>IFaxDoc</b> interface to retrieve and set the properties of a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object.

A client application should not call the <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> function to retrieve an <b>IFaxDoc</b> interface pointer. Instead, the application must perform the following steps to create an instance of a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object: 
                

<ol>
<li>Call the <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> function to retrieve a pointer to an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxserver">IFaxServer</a> interface.</li>
<li>Call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxserver-connect-client-vb">IFaxServer::Connect</a> method to connect to an active fax server. </li>
<li>Call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxserver-createdocument-vb">IFaxServer::CreateDocument</a> method to create and initialize a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object for the connected fax server. (After calling the <b>IFaxServer::CreateDocument</b> method, you can also call the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">IUnknown::QueryInterface</a> method to retrieve an <b>IFaxDoc</b> interface pointer.)</li>
<li>Use the <b>IDispatch</b> interface pointer to call <b>IFaxDoc</b> interface methods.</li>
<li>Call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxserver-disconnect-client-vb">IFaxServer::Disconnect</a> method to disconnect from the fax server.</li>
<li>Call the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method to destroy the <b>IFaxDoc</b> interface pointer, and the parent <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxserver">IFaxServer</a> interface pointer.</li>
</ol>
The property methods of the <b>IFaxDoc</b> interface get or set the properties described following. If the property supports read access, the <b>IFaxDoc</b> interface includes a <i>get_PropertyName</i> method. If the property supports write access, the interface includes a <i>put_PropertyName</i> method.

Values are not required for optional properties that appear only on the cover page. The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-filename-vb">FileName</a> property is required to send a fax transmission using a call to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-send-vb">IFaxDoc::Send</a> method. The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxdoc-get-faxnumber-vb">FaxNumber</a> property is also required.

The fax server can supply data from the registry for many properties that begin with <b>Sender</b>. The fax server supplies values if they have been entered under the <b>User Information</b> tab accessed through the Fax icon in Control Panel.

Following are the properties associated with a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
 

 

