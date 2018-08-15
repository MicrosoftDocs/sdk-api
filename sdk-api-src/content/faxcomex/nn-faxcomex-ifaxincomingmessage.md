---
UID: NN:faxcomex.IFaxIncomingMessage
title: IFaxIncomingMessage
author: windows-sdk-content
description: Used by a fax client application to retrieve information about a received fax message in the archive of inbound faxes.
old-location: fax\_mfax_faxincomingmessage_cpp.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_44h1_cpp.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: IFaxIncomingMessage, IFaxIncomingMessage interface [Fax Service], IFaxIncomingMessage interface [Fax Service],described, _mfax_faxincomingmessage_cpp, fax._mfax_faxincomingmessage_cpp, faxcomex/IFaxIncomingMessage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: faxcomex.h
req.include-header: 
req.redist: 
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

The <b>IFaxIncomingMessage</b> interface is accessed through the <a href="https://msdn.microsoft.com/en-us/library/ms687474(v=VS.85).aspx">IFaxIncomingArchive</a> interface or <a href="https://msdn.microsoft.com/en-us/library/ms687519(v=VS.85).aspx">IFaxIncomingMessageIterator</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxIncomingMessage</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IFaxIncomingMessage</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/ms684905(v=VS.85).aspx">CopyTiff</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms684905(v=VS.85).aspx">CopyTiff</a> method copies the TIFF Class F file associated with the inbound fax message to a file on the local computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms684553(v=VS.85).aspx">Delete</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms684553(v=VS.85).aspx">Delete</a> method deletes the specified fax message from the inbound fax archive.

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

<a href="https://msdn.microsoft.com/en-us/library/ms684807(v=VS.85).aspx">CallerId</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms684807(v=VS.85).aspx">CallerId</a> property is a null-terminated string that identifies the calling device associated with the inbound fax message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/ffac0808-a546-40f5-b38b-28e5998683e3">CSID</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/ffac0808-a546-40f5-b38b-28e5998683e3">CSID</a> property is a null-terminated string that contains the CSID for the inbound fax message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/dfc21bf6-84f6-41a0-9325-110c3b1b8d45">DeviceName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/dfc21bf6-84f6-41a0-9325-110c3b1b8d45">DeviceName</a> property is a null-terminated string that contains the name of the device on which the inbound fax message was received.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/cba22154-22b0-49c9-8246-9b5827ffd162">Id</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/cba22154-22b0-49c9-8246-9b5827ffd162">Id</a> property is a null-terminated string that contains a unique ID for the inbound fax message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms687449(v=VS.85).aspx">Pages</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms687449(v=VS.85).aspx">Pages</a> property is a value that indicates the total number of pages in the inbound fax message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms687457(v=VS.85).aspx">Retries</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms687457(v=VS.85).aspx">Retries</a> property is a value that indicates the number of times that the fax service attempted to route an inbound fax message after the initial routing attempt failed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms684850(v=VS.85).aspx">RoutingInformation</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms684850(v=VS.85).aspx">RoutingInformation</a> property is a null-terminated string that indicates inbound routing information for the fax message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/0d4aca3a-315e-4bc3-aae9-99951bb90128">Size</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/0d4aca3a-315e-4bc3-aae9-99951bb90128">Size</a> property is a value that indicates the size of the TIFF Class F file associated with the inbound fax message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms684560(v=VS.85).aspx">TransmissionEnd</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms684560(v=VS.85).aspx">TransmissionEnd</a> property indicates the time that the inbound fax message completed transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms684556(v=VS.85).aspx">TransmissionStart</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms684556(v=VS.85).aspx">TransmissionStart</a> property indicates the time that the inbound fax message began transmitting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/754a5b45-da88-484b-92fc-ab5906367a8f">TSID</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/754a5b45-da88-484b-92fc-ab5906367a8f">TSID</a> property is a null-terminated string that contains the TSID associated with the inbound fax message.

</td>
</tr>
</table> 


## -remarks



To create a <b>FaxIncomingMessage</b> object in C++, call the <a href="https://msdn.microsoft.com/en-us/library/ms684936(v=VS.85).aspx">IFaxIncomingArchive::GetMessage</a> method or the <a href="https://msdn.microsoft.com/en-us/library/ms687461(v=VS.85).aspx">IFaxIncomingMessageIterator::get_Message</a> method.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms686126(v=VS.85).aspx">FaxIncomingMessage</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/en-us/library/ms687474(v=VS.85).aspx">IFaxIncomingArchive</a>



<a href="https://msdn.microsoft.com/en-us/library/ms687519(v=VS.85).aspx">IFaxIncomingMessageIterator</a>
 

 

