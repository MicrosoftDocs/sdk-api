---
UID: NN:faxcomex.IFaxAccountIncomingArchive
title: IFaxAccountIncomingArchive
author: windows-sdk-content
description: Used by a fax client application to access a particular fax account's archive of successfully received inbound fax messages. Use this interface to retrieve messages and get the size of the archive.
old-location: fax\_mfax_faxaccountincomingarchive_cpp.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccountincomingarchive\faxint_ifaxaccountincomingarchive.htm
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IFaxAccountIncomingArchive, IFaxAccountIncomingArchive interface [Fax Service], IFaxAccountIncomingArchive interface [Fax Service],described, _mfax_faxaccountincomingarchive_cpp, fax._mfax_faxaccountincomingarchive_cpp, faxcomex/IFaxAccountIncomingArchive
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: faxcomex.h
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
 - IFaxAccountIncomingArchive
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxAccountIncomingArchive interface


## -description


Used by a fax client application to access a particular fax account's archive of successfully received inbound fax messages. Use this interface to retrieve messages and get the size of the archive.

A default implementation of <b>IFaxAccountIncomingArchive</b> is provided as the <a href="https://msdn.microsoft.com/d2ae93a1-6325-4b8f-a227-4eb0678702d2">FaxAccountIncomingArchive</a> object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxAccountIncomingArchive</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFaxAccountIncomingArchive</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFaxAccountIncomingArchive</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f9e253ef-1f61-48d5-9f71-7e14ebf538fa">GetMessage</a>
</td>
<td align="left" width="63%">
Returns a fax message from the archive of inbound faxes, for a particular fax account, by using the fax message ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b3469e29-3d98-432b-84bb-2e5a105bf0b0">GetMessages</a>
</td>
<td align="left" width="63%">
Returns a new iterator (archive cursor) for the archive of inbound fax messages for a particular fax account.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ae09646e-70d3-440d-83a0-a38e691b5037">Refresh</a>
</td>
<td align="left" width="63%">
Refreshes <a href="https://msdn.microsoft.com/d2ae93a1-6325-4b8f-a227-4eb0678702d2">FaxAccountIncomingArchive</a> object information for a particular fax account from the fax server. 

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxAccountIncomingArchive</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d88b8ae9-88ce-4ea6-a34d-6d4da4b92b97">SizeHigh</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies the high 32-bit value (in bytes) for the size of the archive of inbound fax messages for a particular fax account.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/947c6fb4-4a67-4c8d-a70c-f23e9ce8e301">SizeLow</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies the low 32-bit value (in bytes) for the size of the archive of inbound fax messages for a particular fax account.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/d2ae93a1-6325-4b8f-a227-4eb0678702d2">FaxAccountIncomingArchive</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

