---
UID: NN:faxcomex.IFaxAccountOutgoingArchive
title: IFaxAccountOutgoingArchive
author: windows-sdk-content
description: Used by a fax client application to access a specified fax account's archive of successfully sent outbound fax messages. Use this interface to retrieve messages and get the size of the archive.
old-location: fax\_mfax_faxaccountoutgoingarchive_cpp.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccountoutgoingarchive\faxint_ifaxaccountoutgoingarchive.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: IFaxAccountOutgoingArchive, IFaxAccountOutgoingArchive interface [Fax Service], IFaxAccountOutgoingArchive interface [Fax Service],described, _mfax_faxaccountoutgoingarchive_cpp, fax._mfax_faxaccountoutgoingarchive_cpp, faxcomex/IFaxAccountOutgoingArchive
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
 - IFaxAccountOutgoingArchive
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxAccountOutgoingArchive interface


## -description


Used by a fax client application to access a specified fax account's archive of successfully sent outbound fax messages. Use this interface to retrieve messages and get the size of the archive.

A default implementation of <b>IFaxAccountOutgoingArchive</b> is provided as the <a href="https://msdn.microsoft.com/21ed0cc8-23a3-4ac1-853f-8f7d004cf843">FaxAccountOutgoingArchive</a> object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxAccountOutgoingArchive</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFaxAccountOutgoingArchive</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFaxAccountOutgoingArchive</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d2d42bb2-72ab-4b9a-bd6f-07f3a5b2ee66">GetMessage</a>
</td>
<td align="left" width="63%">
Returns a fax message from the archive of outbound faxes for a particular fax account, by using the fax message ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/89dd2b73-4ab3-462b-a82a-6288a7c67132">GetMessages</a>
</td>
<td align="left" width="63%">
Returns a new iterator (archive cursor) for the archive of outbound fax messages for a particular fax account.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/96ba0b0b-5099-4ece-a91b-640962e8115c">Refresh</a>
</td>
<td align="left" width="63%">
Refreshes <a href="https://msdn.microsoft.com/21ed0cc8-23a3-4ac1-853f-8f7d004cf843">FaxAccountOutgoingArchive</a> object information for a particular fax account from the fax server. 

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxAccountOutgoingArchive</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/08db8abb-fdd7-40d0-8bb7-d2d54e27a1c8">SizeHigh</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies the high-order 32-bit value of the size (in bytes) of the archive of outbound fax messages for a particular fax account.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/c80efa90-6689-4598-9954-9434674ead99">SizeLow</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies the low-order 32-bit value of the size (in bytes) of the archive of outbound fax messages for a particular fax account.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/21ed0cc8-23a3-4ac1-853f-8f7d004cf843">FaxAccountOutgoingArchive</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

