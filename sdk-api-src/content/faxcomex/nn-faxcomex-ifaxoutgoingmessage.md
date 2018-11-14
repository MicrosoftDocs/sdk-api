---
UID: NN:faxcomex.IFaxOutgoingMessage
title: IFaxOutgoingMessage
author: windows-sdk-content
description: The IFaxOutgoingMessage interface describes an object that is used by a fax client application to retrieve information about a fax message in the archive of outbound faxes.
old-location: fax\_mfax_faxoutgoingmessage_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_8ujp_cpp.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: IFaxOutgoingMessage, IFaxOutgoingMessage interface [Fax Service], IFaxOutgoingMessage interface [Fax Service],described, _mfax_faxoutgoingmessage_cpp, fax._mfax_faxoutgoingmessage_cpp, faxcomex/IFaxOutgoingMessage
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


The <b>IFaxOutgoingMessage</b> interface describes an object that is used by a fax client application to retrieve information about a fax message in the archive of outbound faxes. The archive contains faxes transmitted successfully by the fax service. The object enables you to retrieve information about the fax recipient, contained in the <a href="https://msdn.microsoft.com/e418dbaf-9b07-40a9-bab8-7b4561b63325">FaxRecipient</a> object, and information about the fax sender, contained in the <a href="https://msdn.microsoft.com/f265cfd0-cf62-4d86-9ba5-d1842ac94baa">FaxSender</a> object. It also includes methods to delete a message from the archive and to copy the Tagged Image File Format Class F (TIFF Class F) file associated with the fax message, to a file on the local computer.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxOutgoingMessage</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFaxOutgoingMessage</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/5f45a95e-434f-42e5-be26-f84e21bc94de">CopyTiff</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/5f45a95e-434f-42e5-be26-f84e21bc94de">IFaxOutgoingMessage::CopyTiff</a> method copies the TIFF Class F file associated with the outbound fax message, to a file on the local computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/98799aa3-4100-4865-aadc-60f137873d1f">Delete</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/98799aa3-4100-4865-aadc-60f137873d1f">IFaxOutgoingMessage::Delete</a> method deletes the fax message from the outbound archive.

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

<a href="https://msdn.microsoft.com/27b05cd9-7c5a-4ebd-b5a2-1d1e3c9b9d6e">CSID</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/27b05cd9-7c5a-4ebd-b5a2-1d1e3c9b9d6e">IFaxOutgoingMessage::get_CSID</a> property is a null-terminated string that contains the CSID for the fax message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/0d04289d-706a-420a-8c88-33e17e4bf805">DeviceName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/0d04289d-706a-420a-8c88-33e17e4bf805">IFaxOutgoingMessage::get_DeviceName</a> property is a null-terminated string that contains the name of the device on which the fax message was transmitted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/ec4040b1-b4f2-4f3f-aba4-f51cb8fd2b4b">DocumentName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/ec4040b1-b4f2-4f3f-aba4-f51cb8fd2b4b">IFaxOutgoingMessage::get_DocumentName</a> property is a null-terminated string that contains the user-friendly name to display for the fax message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/a3c70d0f-bb92-44fa-9665-50c01ea76435">Id</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/a3c70d0f-bb92-44fa-9665-50c01ea76435">IFaxOutgoingMessage::get_Id</a> property is a null-terminated string that contains a unique identifier for the outbound fax message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/3157fe56-67a7-4a69-baee-33785d392388">OriginalScheduledTime</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/3157fe56-67a7-4a69-baee-33785d392388">IFaxOutgoingMessage::get_OriginalScheduledTime</a> property specifies the time that the fax message was originally scheduled for transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/cf50a42a-045d-4a12-bb9d-8e70473b4ee3">Pages</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/cf50a42a-045d-4a12-bb9d-8e70473b4ee3">IFaxOutgoingMessage::get_Pages</a> property is a number that indicates the total number of pages in the outbound fax message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/bd727334-0e7a-4f2b-a4bb-2308c9ecfc9a">Priority</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/bd727334-0e7a-4f2b-a4bb-2308c9ecfc9a">IFaxOutgoingMessage::get_Priority</a> property specifies the priority used when sending the fax; for example, normal, low, or high priority.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/a4cb1330-6216-43fb-b158-0f9b9321815e">Recipient</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/a4cb1330-6216-43fb-b158-0f9b9321815e">IFaxOutgoingMessage::get_Recipient</a> property retrieves an interface containing information about the recipient of the fax message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/bc0c32ec-d19c-4eb3-b8a1-1f8c648875e6">Retries</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/bc0c32ec-d19c-4eb3-b8a1-1f8c648875e6">IFaxOutgoingMessage::get_Retries</a> property is a value that indicates the number of times that the fax service attempted to transmit an outgoing fax after the initial transmission attempt failed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/2f02f888-69af-4913-af7b-602afa1d816c">Sender</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/2f02f888-69af-4913-af7b-602afa1d816c">IFaxOutgoingMessage::get_Sender</a> property retrieves an interface containing information about the sender of the fax message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5ae842c8-e063-4d54-a575-b119cc0dcbef">Size</a>


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

<a href="https://msdn.microsoft.com/68700823-a2e7-4630-b996-a4a40fc3e597">Subject</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/68700823-a2e7-4630-b996-a4a40fc3e597">IFaxOutgoingMessage::get_Subject</a> property is a null-terminated string that contains the contents of the subject field on the cover page of the fax.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/b07ffaca-c82f-44c9-b652-660db8cb02a9">SubmissionId</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/b07ffaca-c82f-44c9-b652-660db8cb02a9">IFaxOutgoingMessage::get_SubmissionId</a> property is a null-terminated string that contains the unique identifier assigned to the fax message during the submission process. All fax jobs created by the same submission process share the same unique submission ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/c76a9597-7a8a-4c59-9eb7-fe17f335c5e9">SubmissionTime</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/c76a9597-7a8a-4c59-9eb7-fe17f335c5e9">IFaxOutgoingMessage::get_SubmissionTime</a> property indicates the time that the outbound fax message was submitted for processing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7bbda891-981b-477d-8ddc-9841d6308bf8">TransmissionEnd</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/7bbda891-981b-477d-8ddc-9841d6308bf8">IFaxOutgoingMessage::get_TransmissionEnd</a> property indicates the time that the fax outbound message completed transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/172ef914-9959-4d73-a8f3-90a9091fa538">TransmissionStart</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/172ef914-9959-4d73-a8f3-90a9091fa538">IFaxOutgoingMessage::get_TransmissionStart</a> property indicates the time that the fax outbound message began transmitting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/0d74492b-b504-4c67-a8bd-b23f5814763f">TSID</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/0d74492b-b504-4c67-a8bd-b23f5814763f">IFaxOutgoingMessage::get_TSID</a> property is a null-terminated string that contains the TSID associated with the fax outbound message.

</td>
</tr>
</table> 


## -remarks



A default implementation of <b>IFaxOutgoingMessage</b> is provided as the <a href="https://msdn.microsoft.com/fb06254f-f37b-4783-b4fd-42b5c5a28496">FaxOutgoingMessage</a> object.



