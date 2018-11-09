---
UID: NN:faxcom.IFaxDoc
title: IFaxDoc
author: windows-sdk-content
description: The IFaxDoc dual interface is used by a fax client application to transmit fax documents and cover pages.
old-location: fax\_mfax_ifaxdoc.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_6mub.htm
ms.author: windowssdkdev
ms.date: 11/05/2018
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


The <b>IFaxDoc</b> dual interface is used by a fax client application to transmit fax documents and cover pages. The interface retrieves and sets information about <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> objects. Information includes the name of the file to transmit, the fax number to which the fax server should send the fax, cover page settings, and other optional fax recipient and sender information.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxDoc</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFaxDoc</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/a4c70429-4d1d-4708-acd6-e077bddfbd6c">IFaxDoc::Send</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/a4c70429-4d1d-4708-acd6-e077bddfbd6c">Send</a> method transmits the document specified by the <a href="https://msdn.microsoft.com/fe9f0c64-7722-49ca-809c-5e59acacf474">FileName</a> property of a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object. The method can send the fax to the fax number specified by the <a href="https://msdn.microsoft.com/462ce14c-3440-4e01-919b-9587c19c31a4">FaxNumber</a> property.

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

<a href="https://msdn.microsoft.com/65152957-3f14-4917-b027-00556b6ad8d3">IFaxDoc::get_BillingCode</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/65152957-3f14-4917-b027-00556b6ad8d3">BillingCode</a> property of a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object. The <b>BillingCode</b> property is a null-terminated string that contains an optional billing code that applies to the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9c0fb9e5-fe28-4f77-a967-e6df8c1d2e9d">IFaxDoc::get_CallHandle</a>


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

<a href="https://msdn.microsoft.com/b15a818b-fd37-4958-8fc7-25a8494cdf12">IFaxDoc::get_CoverpageName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/b15a818b-fd37-4958-8fc7-25a8494cdf12">CoverpageName</a> property for a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object. The <b>CoverpageName</b> property is a null-terminated string that contains the name of the cover page template file (.cov) associated with the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7af3638e-b3fa-45a8-a30c-666100b07b6a">IFaxDoc::get_CoverpageNote</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/7af3638e-b3fa-45a8-a30c-666100b07b6a">CoverpageNote</a> property of a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object. The <b>CoverpageNote</b> property is a null-terminated string that contains the text of a message or note from the sender that pertains to the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/36b6352b-0d69-40c8-8906-ed77ab38e2c9">IFaxDoc::get_CoverpageSubject</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/36b6352b-0d69-40c8-8906-ed77ab38e2c9">CoverpageSubject</a> property of a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object. The <b>CoverpageSubject</b> property is a null-terminated string that contains the subject line of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d908fa0c-8fd4-469c-9c4c-b96463b2212e">IFaxDoc::get_DiscountSend</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/d908fa0c-8fd4-469c-9c4c-b96463b2212e">DiscountSend</a> property for a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object. The <b>DiscountSend</b> property is a Boolean value that indicates whether the fax server transmits faxes during the discount period.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/27e983b9-0d24-42ec-a0f3-dd0723766c4c">IFaxDoc::get_DisplayName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/27e983b9-0d24-42ec-a0f3-dd0723766c4c">DisplayName</a> property of a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object. The <b>DisplayName</b> property is a null-terminated string that contains the name to associate with the fax document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e921db9c-de5c-42f4-a17a-0ad50b5ab787">IFaxDoc::get_EmailAddress</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/e921db9c-de5c-42f4-a17a-0ad50b5ab787">EmailAddress</a> property of a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object. The <b>EmailAddress</b> property is a null-terminated string that contains the email address of the sender of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/462ce14c-3440-4e01-919b-9587c19c31a4">IFaxDoc::get_FaxNumber</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/462ce14c-3440-4e01-919b-9587c19c31a4">FaxNumber</a> property of a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object. The <b>FaxNumber</b> property is a null-terminated string that contains the fax number to which the fax server will send the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/fe9f0c64-7722-49ca-809c-5e59acacf474">IFaxDoc::get_FileName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/fe9f0c64-7722-49ca-809c-5e59acacf474">FileName</a> property for a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object. The <b>FileName</b> property is a null-terminated string that contains the name of the document file associated with the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5004bd2c-ee6f-42f7-b638-2b52c0ffba2f">IFaxDoc::get_RecipientAddress</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/5004bd2c-ee6f-42f7-b638-2b52c0ffba2f">RecipientAddress</a> property of a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object. The <b>RecipientAddress</b> property is a null-terminated string that contains the street address of the recipient of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/2c53cd96-16fe-4434-9a85-3b629840e302">IFaxDoc::get_RecipientCity</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/2c53cd96-16fe-4434-9a85-3b629840e302">RecipientCity</a> property of a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object. The <b>RecipientCity</b> property is a null-terminated string that contains the city name of the recipient of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9d06b3a3-3581-4d25-9f06-f9c9dcbecd44">IFaxDoc::get_RecipientCompany</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/9d06b3a3-3581-4d25-9f06-f9c9dcbecd44">RecipientCompany</a> property of a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object. The <b>RecipientCompany</b> property is a null-terminated string that contains the company name of the recipient of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93ee1709-1cdb-454f-ac36-eab95da6f58b">IFaxDoc::get_RecipientCountry</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/93ee1709-1cdb-454f-ac36-eab95da6f58b">RecipientCountry</a> property of a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object. The <b>RecipientCountry</b> property is a null-terminated string that contains the country/region of the recipient of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/a766f9b6-b119-4bca-acdb-38686bd3ce47">IFaxDoc::get_RecipientDepartment</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/a766f9b6-b119-4bca-acdb-38686bd3ce47">RecipientDepartment</a> property of a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object. The <b>RecipientDepartment</b> property is a null-terminated string that contains the department of the recipient of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7e65c7e2-24b7-4f60-bbd7-abf2bcfce38e">IFaxDoc::get_RecipientHomePhone</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/7e65c7e2-24b7-4f60-bbd7-abf2bcfce38e">RecipientHomePhone</a> property of a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object. The <b>RecipientHomePhone</b> property is a null-terminated string that contains the home telephone number of the recipient of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/a8522a6d-a55f-4cd3-9b71-53bb5109a84d">IFaxDoc::get_RecipientName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/a8522a6d-a55f-4cd3-9b71-53bb5109a84d">RecipientName</a> property of a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object. The <b>RecipientName</b> property is a null-terminated string that contains the name of the recipient of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/56613e6c-6701-47cf-9595-153e1e87373d">IFaxDoc::get_RecipientOffice</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/56613e6c-6701-47cf-9595-153e1e87373d">RecipientOffice</a> property of a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object. The <b>RecipientOffice</b> property is a null-terminated string that contains the office of the recipient of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/1caad1a4-d3a7-44cd-8328-1291c71f8975">IFaxDoc::get_RecipientOfficePhone</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/1caad1a4-d3a7-44cd-8328-1291c71f8975">RecipientOfficePhone</a> property of a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object. The <b>RecipientOfficePhone</b> property is a null-terminated string that contains the office telephone number of the recipient of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/fe7caea6-5d93-4444-9133-9e5d4f6e624e">IFaxDoc::get_RecipientState</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/fe7caea6-5d93-4444-9133-9e5d4f6e624e">RecipientState</a> property of a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object. The <b>RecipientState</b> property is a null-terminated string that contains the state of the recipient of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/a721eb3c-d0ec-4438-b8a6-b208f5532eb7">IFaxDoc::get_RecipientTitle</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/a721eb3c-d0ec-4438-b8a6-b208f5532eb7">RecipientTitle</a> property of a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object. The <b>RecipientTitle</b> property is a null-terminated string that contains the title of the recipient of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/c42aac37-28c5-4045-80a8-df5bb194b202">IFaxDoc::get_RecipientZip</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/c42aac37-28c5-4045-80a8-df5bb194b202">RecipientZip</a> property of a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object. The <b>RecipientZip</b> property is a null-terminated string that contains the ZIP code of the recipient of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9bf1dd42-bdc9-4bb9-b5e0-3a0934b0001b">IFaxDoc::get_SendCoverpage</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/9bf1dd42-bdc9-4bb9-b5e0-3a0934b0001b">SendCoverpage</a> property for a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object. The <b>SendCoverpage</b> property is a Boolean value that indicates whether the specified cover page file is stored on the fax server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/100d5d50-b45c-4842-944a-bc129b369ff7">IFaxDoc::get_SenderAddress</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/100d5d50-b45c-4842-944a-bc129b369ff7">SenderAddress</a> property of a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object. The <b>SenderAddress</b> property is a null-terminated string that contains the street address of the sender of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/debb69a7-fa3f-45ce-ab05-6bd757a9e509">IFaxDoc::get_SenderCompany</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/debb69a7-fa3f-45ce-ab05-6bd757a9e509">SenderCompany</a> property of a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object. The <b>SenderCompany</b> property is a null-terminated string that contains the company name of the sender of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/821b95a1-2096-4177-9794-31d3187c30d8">IFaxDoc::get_SenderDepartment</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/821b95a1-2096-4177-9794-31d3187c30d8">SenderDepartment</a> property of a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object. The <b>SenderDepartment</b> property is a null-terminated string that contains the department of the sender of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/a884bcf2-5769-45d7-b112-6550e57e52ed">IFaxDoc::get_SenderFax</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/a884bcf2-5769-45d7-b112-6550e57e52ed">SenderFax</a> property of a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object. The <b>SenderFax</b> property is a null-terminated string that contains the fax number of the sender of the outbound fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/963104a8-459e-49a8-ac33-d1184d4fc442">IFaxDoc::get_SenderHomePhone</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/963104a8-459e-49a8-ac33-d1184d4fc442">SenderHomePhone</a> property of a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object. The <b>SenderHomePhone</b> property is a null-terminated string that contains the home telephone number of the sender of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/298b85b1-4af1-4fc5-9572-b8c1e88a5d6d">IFaxDoc::get_SenderName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/298b85b1-4af1-4fc5-9572-b8c1e88a5d6d">SenderName</a> property of a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object. The <b>SenderName</b> property is a null-terminated string that contains the name of the sender of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/71acb678-2be9-4247-92b7-858b86cb06f3">IFaxDoc::get_SenderOffice</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/71acb678-2be9-4247-92b7-858b86cb06f3">SenderOffice</a> property of a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object. The <b>SenderOffice</b> property is a null-terminated string that contains the office of the sender of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7a9b81aa-bfa3-41b0-b5b5-372390aa7dd0">IFaxDoc::get_SenderOfficePhone</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/7a9b81aa-bfa3-41b0-b5b5-372390aa7dd0">SenderOfficePhone</a> property of a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object. The <b>SenderOfficePhone</b> property is a null-terminated string that contains the office telephone number of the sender of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7fe47534-da3c-4997-bb94-4f20c2a0ebd7">IFaxDoc::get_SenderTitle</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/7fe47534-da3c-4997-bb94-4f20c2a0ebd7">SenderTitle</a> property of a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object. The <b>SenderTitle</b> property is a null-terminated string that contains the title of the sender of the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/c7571a29-c145-4ab6-976e-547f9491cf1f">IFaxDoc::get_ServerCoverpage</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/c7571a29-c145-4ab6-976e-547f9491cf1f">ServerCoverpage</a> property for a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object. The <b>ServerCoverpage</b> property is a Boolean value that indicates whether the specified cover page file is stored on the fax server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/26d33ea3-a30d-4a04-9760-f637196db23d">IFaxDoc::get_Tsid</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/26d33ea3-a30d-4a04-9760-f637196db23d">Tsid</a> property of a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object. The <b>Tsid</b> property is a null-terminated string that contains a user-defined TSID.

</td>
</tr>
</table> 


## -remarks



The <b>IFaxDoc</b> interface includes the following methods:

<ul>
<li>A method to send a fax document.</li>
<li>Property methods to set and retrieve individual property values associated with a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object.</li>
</ul>
<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
You should not implement this interface. The Microsoft standard implementation provides complete functionality.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Use the <b>IFaxDoc</b> interface to send a fax document. You can also use the <b>IFaxDoc</b> interface to retrieve and set the properties of a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object.

A client application should not call the <a href="_com_CoCreateInstance">CoCreateInstance</a> function to retrieve an <b>IFaxDoc</b> interface pointer. Instead, the application must perform the following steps to create an instance of a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object: 
                

<ol>
<li>Call the <a href="_com_CoCreateInstance">CoCreateInstance</a> function to retrieve a pointer to an <a href="https://msdn.microsoft.com/f06b76b5-b6c2-47a0-ad08-7c1bf7b780bb">IFaxServer</a> interface.</li>
<li>Call the <a href="https://msdn.microsoft.com/12e71c4c-c4b5-4e6d-a1fa-b833d6a00ff8">IFaxServer::Connect</a> method to connect to an active fax server. </li>
<li>Call the <a href="https://msdn.microsoft.com/5132538b-8250-4279-8091-19f112176594">IFaxServer::CreateDocument</a> method to create and initialize a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object for the connected fax server. (After calling the <b>IFaxServer::CreateDocument</b> method, you can also call the <a href="_com_IUnknown_QueryInterface">IUnknown::QueryInterface</a> method to retrieve an <b>IFaxDoc</b> interface pointer.)</li>
<li>Use the <b>IDispatch</b> interface pointer to call <b>IFaxDoc</b> interface methods.</li>
<li>Call the <a href="https://msdn.microsoft.com/dccbb6b1-b889-4b73-a3d0-9c5ce6268f4a">IFaxServer::Disconnect</a> method to disconnect from the fax server.</li>
<li>Call the <a href="_com_IUnknown_Release">IUnknown::Release</a> method to destroy the <b>IFaxDoc</b> interface pointer, and the parent <a href="https://msdn.microsoft.com/f06b76b5-b6c2-47a0-ad08-7c1bf7b780bb">IFaxServer</a> interface pointer.</li>
</ol>
The property methods of the <b>IFaxDoc</b> interface get or set the properties described following. If the property supports read access, the <b>IFaxDoc</b> interface includes a <i>get_PropertyName</i> method. If the property supports write access, the interface includes a <i>put_PropertyName</i> method.

Values are not required for optional properties that appear only on the cover page. The <a href="https://msdn.microsoft.com/fe9f0c64-7722-49ca-809c-5e59acacf474">FileName</a> property is required to send a fax transmission using a call to the <a href="https://msdn.microsoft.com/a4c70429-4d1d-4708-acd6-e077bddfbd6c">IFaxDoc::Send</a> method. The <a href="https://msdn.microsoft.com/462ce14c-3440-4e01-919b-9587c19c31a4">FaxNumber</a> property is also required.

The fax server can supply data from the registry for many properties that begin with <b>Sender</b>. The fax server supplies values if they have been entered under the <b>User Information</b> tab accessed through the Fax icon in Control Panel.

Following are the properties associated with a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object.




## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

