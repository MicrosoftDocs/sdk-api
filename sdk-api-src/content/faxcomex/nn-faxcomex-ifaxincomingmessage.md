---
UID: NN:faxcomex.IFaxIncomingMessage
title: IFaxIncomingMessage
author: windows-sdk-content
description: Used by a fax client application to retrieve information about a received fax message in the archive of inbound faxes.
old-location: fax\_mfax_faxincomingmessage_cpp.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_44h1_cpp.htm
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: IFaxIncomingMessage, IFaxIncomingMessage interface [Fax Service], IFaxIncomingMessage interface [Fax Service],described, _mfax_faxincomingmessage_cpp, fax._mfax_faxincomingmessage_cpp, faxcomex/IFaxIncomingMessage
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
 - IFaxIncomingMessage
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxIncomingMessage interface


## -description


Used by a fax client application to retrieve information about a received fax message in the archive of inbound faxes. The archive contains faxes received successfully by the fax service. The interface also includes methods to delete a message from the archive and to copy the Tagged Image File Format Class F (TIFF Class F) file associated with the fax message to a file on the local computer.

The <b>IFaxIncomingMessage</b> interface is accessed through the <a href="https://msdn.microsoft.com/0442fc06-20b8-4608-8532-c8901832f39b">IFaxIncomingArchive</a> interface or <a href="https://msdn.microsoft.com/f0b3071b-6936-4b19-873b-0ab28cfaea93">IFaxIncomingMessageIterator</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxIncomingMessage</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFaxIncomingMessage</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFaxIncomingMessage</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b48762b8-d556-497d-be91-bad3a4908a8d">CopyTiff</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/b48762b8-d556-497d-be91-bad3a4908a8d">CopyTiff</a> method copies the TIFF Class F file associated with the inbound fax message to a file on the local computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/86e1f59e-5abe-4734-a736-0ef71d8d3ce1">Delete</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/86e1f59e-5abe-4734-a736-0ef71d8d3ce1">Delete</a> method deletes the specified fax message from the inbound fax archive.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxIncomingMessage</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/17904bd7-e63a-4ed3-94ee-eae2e2d96fb4">CallerId</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/17904bd7-e63a-4ed3-94ee-eae2e2d96fb4">CallerId</a> property is a null-terminated string that identifies the calling device associated with the inbound fax message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn922691">CSID</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/library/windows/hardware/dn922691">CSID</a> property is a null-terminated string that contains the CSID for the inbound fax message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/mt188594">DeviceName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/library/windows/hardware/mt188594">DeviceName</a> property is a null-terminated string that contains the name of the device on which the inbound fax message was received.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn895599">Id</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/library/windows/hardware/dn895599">Id</a> property is a null-terminated string that contains a unique ID for the inbound fax message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/ed0fe64a-7c8e-4024-99ce-c79a665c6bf7">Pages</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/ed0fe64a-7c8e-4024-99ce-c79a665c6bf7">Pages</a> property is a value that indicates the total number of pages in the inbound fax message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/add90176-d267-4697-af18-f2283b3cbd28">Retries</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/add90176-d267-4697-af18-f2283b3cbd28">Retries</a> property is a value that indicates the number of times that the fax service attempted to route an inbound fax message after the initial routing attempt failed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/fe0391d3-d4f2-4fb4-a60a-6e04f1930355">RoutingInformation</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/fe0391d3-d4f2-4fb4-a60a-6e04f1930355">RoutingInformation</a> property is a null-terminated string that indicates inbound routing information for the fax message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn915850">Size</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/library/windows/hardware/dn915850">Size</a> property is a value that indicates the size of the TIFF Class F file associated with the inbound fax message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/22b2696c-6bcd-44e5-b595-c23824a953f2">TransmissionEnd</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/22b2696c-6bcd-44e5-b595-c23824a953f2">TransmissionEnd</a> property indicates the time that the inbound fax message completed transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/22f07bdf-aaeb-4d15-b4e6-5027a86a4ca2">TransmissionStart</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/22f07bdf-aaeb-4d15-b4e6-5027a86a4ca2">TransmissionStart</a> property indicates the time that the inbound fax message began transmitting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn997387">TSID</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/library/windows/hardware/dn997387">TSID</a> property is a null-terminated string that contains the TSID associated with the inbound fax message.

</td>
</tr>
</table> 


## -remarks



To create a <b>FaxIncomingMessage</b> object in C++, call the <a href="https://msdn.microsoft.com/250f7040-30ab-45c5-8d6f-307c7d0b4d84">IFaxIncomingArchive::GetMessage</a> method or the <a href="https://msdn.microsoft.com/52846cf4-4e6b-43cc-a9ba-3e4820fc2aa8">IFaxIncomingMessageIterator::get_Message</a> method.




## -see-also




<a href="https://msdn.microsoft.com/ee546d4c-e580-4738-a5d2-0b10c5d8a1ab">FaxIncomingMessage</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/0442fc06-20b8-4608-8532-c8901832f39b">IFaxIncomingArchive</a>



<a href="https://msdn.microsoft.com/f0b3071b-6936-4b19-873b-0ab28cfaea93">IFaxIncomingMessageIterator</a>
 

 

