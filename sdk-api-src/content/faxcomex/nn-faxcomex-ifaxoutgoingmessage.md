---
UID: NN:faxcomex.IFaxOutgoingMessage
title: IFaxOutgoingMessage (faxcomex.h)
author: windows-sdk-content
description: The IFaxOutgoingMessage interface describes an object that is used by a fax client application to retrieve information about a fax message in the archive of outbound faxes.
old-location: fax\_mfax_faxoutgoingmessage_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_8ujp_cpp.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxOutgoingMessage, IFaxOutgoingMessage interface [Fax Service], IFaxOutgoingMessage interface [Fax Service],described, _mfax_faxoutgoingmessage_cpp, fax._mfax_faxoutgoingmessage_cpp, faxcomex/IFaxOutgoingMessage
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
 - IFaxOutgoingMessage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxOutgoingMessage interface


## -description


The <b>IFaxOutgoingMessage</b> interface describes an object that is used by a fax client application to retrieve information about a fax message in the archive of outbound faxes. The archive contains faxes transmitted successfully by the fax service. The object enables you to retrieve information about the fax recipient, contained in the <a href="https://msdn.microsoft.com/en-us/library/ms690204(v=VS.85).aspx">FaxRecipient</a> object, and information about the fax sender, contained in the <a href="https://msdn.microsoft.com/en-us/library/ms687532(v=VS.85).aspx">FaxSender</a> object. It also includes methods to delete a message from the archive and to copy the Tagged Image File Format Class F (TIFF Class F) file associated with the fax message, to a file on the local computer.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxOutgoingMessage</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IFaxOutgoingMessage</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFaxOutgoingMessage</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms687991(v=VS.85).aspx">CopyTiff</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms687991(v=VS.85).aspx">IFaxOutgoingMessage::CopyTiff</a> method copies the TIFF Class F file associated with the outbound fax message, to a file on the local computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms687526(v=VS.85).aspx">Delete</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms687526(v=VS.85).aspx">IFaxOutgoingMessage::Delete</a> method deletes the fax message from the outbound archive.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxOutgoingMessage</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms690159(v=VS.85).aspx">CSID</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms690159(v=VS.85).aspx">IFaxOutgoingMessage::get_CSID</a> property is a null-terminated string that contains the CSID for the fax message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms687548(v=VS.85).aspx">DeviceName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms687548(v=VS.85).aspx">IFaxOutgoingMessage::get_DeviceName</a> property is a null-terminated string that contains the name of the device on which the fax message was transmitted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms688249(v=VS.85).aspx">DocumentName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms688249(v=VS.85).aspx">IFaxOutgoingMessage::get_DocumentName</a> property is a null-terminated string that contains the user-friendly name to display for the fax message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms688575(v=VS.85).aspx">Id</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms688575(v=VS.85).aspx">IFaxOutgoingMessage::get_Id</a> property is a null-terminated string that contains a unique identifier for the outbound fax message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms690183(v=VS.85).aspx">OriginalScheduledTime</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms690183(v=VS.85).aspx">IFaxOutgoingMessage::get_OriginalScheduledTime</a> property specifies the time that the fax message was originally scheduled for transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms687982(v=VS.85).aspx">Pages</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms687982(v=VS.85).aspx">IFaxOutgoingMessage::get_Pages</a> property is a number that indicates the total number of pages in the outbound fax message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms690170(v=VS.85).aspx">Priority</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms690170(v=VS.85).aspx">IFaxOutgoingMessage::get_Priority</a> property specifies the priority used when sending the fax; for example, normal, low, or high priority.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms689201(v=VS.85).aspx">Recipient</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms689201(v=VS.85).aspx">IFaxOutgoingMessage::get_Recipient</a> property retrieves an interface containing information about the recipient of the fax message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms689587(v=VS.85).aspx">Retries</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms689587(v=VS.85).aspx">IFaxOutgoingMessage::get_Retries</a> property is a value that indicates the number of times that the fax service attempted to transmit an outgoing fax after the initial transmission attempt failed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms688010(v=VS.85).aspx">Sender</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms688010(v=VS.85).aspx">IFaxOutgoingMessage::get_Sender</a> property retrieves an interface containing information about the sender of the fax message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms690042(v=VS.85).aspx">Size</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The Size property is a value that indicates the size of the TIFF Class F file associated with the outbound fax message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms687534(v=VS.85).aspx">Subject</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms687534(v=VS.85).aspx">IFaxOutgoingMessage::get_Subject</a> property is a null-terminated string that contains the contents of the subject field on the cover page of the fax.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms689189(v=VS.85).aspx">SubmissionId</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms689189(v=VS.85).aspx">IFaxOutgoingMessage::get_SubmissionId</a> property is a null-terminated string that contains the unique identifier assigned to the fax message during the submission process. All fax jobs created by the same submission process share the same unique submission ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms687539(v=VS.85).aspx">SubmissionTime</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms687539(v=VS.85).aspx">IFaxOutgoingMessage::get_SubmissionTime</a> property indicates the time that the outbound fax message was submitted for processing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms690174(v=VS.85).aspx">TransmissionEnd</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms690174(v=VS.85).aspx">IFaxOutgoingMessage::get_TransmissionEnd</a> property indicates the time that the fax outbound message completed transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms690059(v=VS.85).aspx">TransmissionStart</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms690059(v=VS.85).aspx">IFaxOutgoingMessage::get_TransmissionStart</a> property indicates the time that the fax outbound message began transmitting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms689104(v=VS.85).aspx">TSID</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms689104(v=VS.85).aspx">IFaxOutgoingMessage::get_TSID</a> property is a null-terminated string that contains the TSID associated with the fax outbound message.

</td>
</tr>
</table> 


## -remarks



A default implementation of <b>IFaxOutgoingMessage</b> is provided as the <a href="https://msdn.microsoft.com/en-us/library/ms690149(v=VS.85).aspx">FaxOutgoingMessage</a> object.



