---
UID: NN:faxcomex.IFaxReceiptOptions
title: IFaxReceiptOptions
author: windows-sdk-content
description: The IFaxReceiptOptions interface defines a FaxReceiptOptions configuration object used by a fax client application to set and retrieve the receipt configuration that the fax service uses to send delivery receipts for fax transmissions.
old-location: fax\_mfax_faxreceiptoptions_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_8k4z_cpp.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IFaxReceiptOptions, IFaxReceiptOptions interface [Fax Service], IFaxReceiptOptions interface [Fax Service],described, _mfax_faxreceiptoptions_cpp, fax._mfax_faxreceiptoptions_cpp, faxcomex/IFaxReceiptOptions
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
 - IFaxReceiptOptions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxReceiptOptions interface


## -description


The <b>IFaxReceiptOptions</b> interface defines a <a href="https://msdn.microsoft.com/en-us/library/ms690118(v=VS.85).aspx">FaxReceiptOptions</a> configuration object used by a fax client application to set and retrieve the receipt configuration that the fax service uses to send delivery receipts for fax transmissions. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxReceiptOptions</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IFaxReceiptOptions</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFaxReceiptOptions</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms689562(v=VS.85).aspx">Refresh</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms689562(v=VS.85).aspx">IFaxReceiptOptions::Refresh</a> method refreshes <a href="https://msdn.microsoft.com/en-us/library/ms690118(v=VS.85).aspx">FaxReceiptOptions</a> object information from the fax server. When the <b>IFaxReceiptOptions::Refresh</b> method is called, any configuration changes made after the last <a href="https://msdn.microsoft.com/en-us/library/ms688388(v=VS.85).aspx">IFaxReceiptOptions::Save</a> method call are lost.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms688388(v=VS.85).aspx">Save</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms688388(v=VS.85).aspx">IFaxReceiptOptions::Save</a> method saves the <a href="https://msdn.microsoft.com/en-us/library/ms690118(v=VS.85).aspx">FaxReceiptOptions</a> object data.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxReceiptOptions</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms688638(v=VS.85).aspx">AllowedReceipts</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms688638(v=VS.85).aspx">IFaxReceiptOptions::get_AllowedReceipts</a> property is a value that specifies the permitted types of delivery receipts.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms689591(v=VS.85).aspx">AuthenticationType</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms689591(v=VS.85).aspx">IFaxReceiptOptions::get_AuthenticationType</a> property specifies the type of authentication the fax service uses when connecting to an SMTP server. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms687995(v=VS.85).aspx">SMTPPassword</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms687995(v=VS.85).aspx">IFaxReceiptOptions::get_SMTPPassword</a> property is a null-terminated string that contains the SMTP password used for authenticated connections.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms689608(v=VS.85).aspx">SMTPPort</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms689608(v=VS.85).aspx">IFaxReceiptOptions::get_SMTPPort</a> property is a value that specifies the SMTP port number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms689076(v=VS.85).aspx">SMTPSender</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms689076(v=VS.85).aspx">IFaxReceiptOptions::get_SMTPSender</a> property is a null-terminated string that contains the SMTP email address for the sender of the mail message receipt.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms690055(v=VS.85).aspx">SMTPServer</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms690055(v=VS.85).aspx">IFaxReceiptOptions::get_SMTPServer</a> property is a null-terminated string that contains the name of the SMTP server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms689521(v=VS.85).aspx">SMTPUser</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms689521(v=VS.85).aspx">IFaxReceiptOptions::get_SMTPUser</a> property is a null-terminated string that contains the SMTP user name used for authenticated connections. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms689610(v=VS.85).aspx">UseForInboundRouting </a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms689610(v=VS.85).aspx">IFaxReceiptOptions::get_UseForInboundRouting </a> property sets or retrieves whether to use the <a href="https://msdn.microsoft.com/en-us/library/ms690118(v=VS.85).aspx">FaxReceiptOptions</a> settings for the Microsoft Routing Extension, which allows incoming faxes to be routed to email addresses. 

</td>
</tr>
</table> 


## -remarks



A default implementation of <b>IFaxReceiptOptions</b> is provided as the <a href="https://msdn.microsoft.com/en-us/library/ms690118(v=VS.85).aspx">FaxReceiptOptions</a> object. 



