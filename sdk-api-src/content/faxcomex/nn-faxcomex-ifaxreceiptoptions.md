---
UID: NN:faxcomex.IFaxReceiptOptions
title: IFaxReceiptOptions
author: windows-driver-content
description: The IFaxReceiptOptions interface defines a FaxReceiptOptions configuration object used by a fax client application to set and retrieve the receipt configuration that the fax service uses to send delivery receipts for fax transmissions.
old-location: fax\_mfax_faxreceiptoptions_cpp.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_8k4z_cpp.htm
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IFaxReceiptOptions, IFaxReceiptOptions interface [Fax Service], IFaxReceiptOptions interface [Fax Service],described, _mfax_faxreceiptoptions_cpp, fax._mfax_faxreceiptoptions_cpp, faxcomex/IFaxReceiptOptions
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Fxscomex.dll
api_name:
-	IFaxReceiptOptions
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxReceiptOptions interface


## -description


The <b>IFaxReceiptOptions</b> interface defines a <a href="https://msdn.microsoft.com/6c3d1358-6819-42e3-9be0-896ed7e2d463">FaxReceiptOptions</a> configuration object used by a fax client application to set and retrieve the receipt configuration that the fax service uses to send delivery receipts for fax transmissions. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxReceiptOptions</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFaxReceiptOptions</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/f14c67ec-a16f-414d-ac2b-62a9f09acf8b">Refresh</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/f14c67ec-a16f-414d-ac2b-62a9f09acf8b">IFaxReceiptOptions::Refresh</a> method refreshes <a href="https://msdn.microsoft.com/6c3d1358-6819-42e3-9be0-896ed7e2d463">FaxReceiptOptions</a> object information from the fax server. When the <b>IFaxReceiptOptions::Refresh</b> method is called, any configuration changes made after the last <a href="https://msdn.microsoft.com/dc884156-1427-4b4f-bf2b-2705d2622635">IFaxReceiptOptions::Save</a> method call are lost.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926944">Save</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/dc884156-1427-4b4f-bf2b-2705d2622635">IFaxReceiptOptions::Save</a> method saves the <a href="https://msdn.microsoft.com/6c3d1358-6819-42e3-9be0-896ed7e2d463">FaxReceiptOptions</a> object data.

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

<a href="https://msdn.microsoft.com/2b2ecbf5-aeed-4d6f-8849-effcea0f9972">AllowedReceipts</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/2b2ecbf5-aeed-4d6f-8849-effcea0f9972">IFaxReceiptOptions::get_AllowedReceipts</a> property is a value that specifies the permitted types of delivery receipts.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/1624ad8c-07ca-4ab1-970c-fb0624903b81">AuthenticationType</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/1624ad8c-07ca-4ab1-970c-fb0624903b81">IFaxReceiptOptions::get_AuthenticationType</a> property specifies the type of authentication the fax service uses when connecting to an SMTP server. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/c290a5de-e2ce-4349-82ba-a61929cf0db2">SMTPPassword</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/c290a5de-e2ce-4349-82ba-a61929cf0db2">IFaxReceiptOptions::get_SMTPPassword</a> property is a null-terminated string that contains the SMTP password used for authenticated connections.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/cb2e1464-2e1e-48c3-a62a-7c42ab38f549">SMTPPort</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/cb2e1464-2e1e-48c3-a62a-7c42ab38f549">IFaxReceiptOptions::get_SMTPPort</a> property is a value that specifies the SMTP port number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d6f4a3f3-e847-4b62-96bb-763daad9245b">SMTPSender</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/d6f4a3f3-e847-4b62-96bb-763daad9245b">IFaxReceiptOptions::get_SMTPSender</a> property is a null-terminated string that contains the SMTP email address for the sender of the mail message receipt.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7170cfc4-c201-4544-9e4d-ff0394789810">SMTPServer</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/7170cfc4-c201-4544-9e4d-ff0394789810">IFaxReceiptOptions::get_SMTPServer</a> property is a null-terminated string that contains the name of the SMTP server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/3f61747e-a54a-4137-b7fe-c170e940a118">SMTPUser</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/3f61747e-a54a-4137-b7fe-c170e940a118">IFaxReceiptOptions::get_SMTPUser</a> property is a null-terminated string that contains the SMTP user name used for authenticated connections. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/ac1a3bde-d729-4669-b7e1-40bd6a00f921">UseForInboundRouting </a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/ac1a3bde-d729-4669-b7e1-40bd6a00f921">IFaxReceiptOptions::get_UseForInboundRouting </a> property sets or retrieves whether to use the <a href="https://msdn.microsoft.com/6c3d1358-6819-42e3-9be0-896ed7e2d463">FaxReceiptOptions</a> settings for the Microsoft Routing Extension, which allows incoming faxes to be routed to email addresses. 

</td>
</tr>
</table> 


## -remarks



A default implementation of <b>IFaxReceiptOptions</b> is provided as the <a href="https://msdn.microsoft.com/6c3d1358-6819-42e3-9be0-896ed7e2d463">FaxReceiptOptions</a> object. 



