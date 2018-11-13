---
UID: NN:faxcomex.IFaxOutgoingJob
title: IFaxOutgoingJob
author: windows-sdk-content
description: The IFaxOutgoingJob interface describes an object that is used by a fax client application to retrieve information about an outgoing fax job in a fax server's queue.
old-location: fax\_mfax_faxoutgoingjob_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_4mjm_cpp.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: IFaxOutgoingJob, IFaxOutgoingJob interface [Fax Service], IFaxOutgoingJob interface [Fax Service],described, _mfax_faxoutgoingjob_cpp, fax._mfax_faxoutgoingjob_cpp, faxcomex/IFaxOutgoingJob
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
 - IFaxOutgoingJob
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxOutgoingJob interface


## -description


The <b>IFaxOutgoingJob</b> interface describes an object that is used by a fax client application to retrieve information about an outgoing fax job in a fax server's queue. The object also includes methods to cancel, pause, resume, or restart an outgoing fax job, and to copy the Tagged Image File Format Class F (TIFF Class F) file associated with an outbound fax job, to a file on the local computer.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxOutgoingJob</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFaxOutgoingJob</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFaxOutgoingJob</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42f53e47-32bb-4888-bdcf-d05e12fc9859">Cancel</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/42f53e47-32bb-4888-bdcf-d05e12fc9859">IFaxOutgoingJob::Cancel</a> method cancels the outbound fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f40c487e-d7af-49c7-b0f5-7e1c8297fd86">CopyTiff</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/f40c487e-d7af-49c7-b0f5-7e1c8297fd86">IFaxOutgoingJob::CopyTiff</a> method copies the TIFF Class F file associated with the outbound fax job, to a file on the local computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d709fd69-d34b-4dca-aea0-7726698a7dca">Pause</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/d709fd69-d34b-4dca-aea0-7726698a7dca">IFaxOutgoingJob::Pause</a> method pauses the outbound fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/53b02fd1-302b-476d-a467-de94cc14a0c0">Refresh</a>
</td>
<td align="left" width="63%">
The Refresh method refreshes <a href="https://msdn.microsoft.com/f9686d11-fd32-4eaf-ae93-399dacf028ac">FaxOutgoingJob</a> object information from the fax server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/524d5788-0e39-4501-9a52-2866c8887d80">Restart</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/524d5788-0e39-4501-9a52-2866c8887d80">IFaxOutgoingJob::Restart</a> method restarts the failed outbound fax job. For example, if the fax job has exceeded the number of retries, <b>IFaxOutgoingJob::Restart</b> will restart the fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2893d8fc-0d11-4a78-9b67-a37c43b58955">Resume</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/2893d8fc-0d11-4a78-9b67-a37c43b58955">IFaxOutgoingJob::Resume</a> method resumes the paused outbound fax job.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxOutgoingJob</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/4d97ef95-77d0-4616-afcd-7adbc26ff3c5">AvailableOperations</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/4d97ef95-77d0-4616-afcd-7adbc26ff3c5">IFaxOutgoingJob::get_AvailableOperations</a> property indicates the combination of valid operations that you can perform on the fax job, given its current status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/40c477a8-74dd-4e5a-8d1e-f17b77e77012">CSID</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/40c477a8-74dd-4e5a-8d1e-f17b77e77012">IFaxOutgoingJob::get_CSID</a> property is a null-terminated string that contains the CSID associated with the fax outbound job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/53d776c5-581f-445c-82fa-551a3c34f6c3">CurrentPage</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/53d776c5-581f-445c-82fa-551a3c34f6c3">IFaxOutgoingJob::get_CurrentPage</a> property is a number that identifies the page that the fax service is actively transmitting on an outbound fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/f4366dee-4201-4ee5-8a41-94717f9b0960">DeviceId</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/f4366dee-4201-4ee5-8a41-94717f9b0960">IFaxOutgoingJob::get_DeviceId</a> property indicates the device ID of the device transmitting the outbound fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/aec728cf-38b5-49f9-943c-aa907d05fe21">DocumentName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/aec728cf-38b5-49f9-943c-aa907d05fe21">IFaxOutgoingJob::get_DocumentName</a> property is a null-terminated string that contains the user-friendly name to display for the fax document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8b397aa9-aca0-4da2-9afa-cff0933d5f78">ExtendedStatus</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/8b397aa9-aca0-4da2-9afa-cff0933d5f78">IFaxOutgoingJob::get_ExtendedStatus</a> property is a null-terminated string that describes the job's extended status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/f2014b38-b5dd-48bd-a391-457de69bd7b4">ExtendedStatusCode</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/f2014b38-b5dd-48bd-a391-457de69bd7b4">IFaxOutgoingJob::get_ExtendedStatusCode</a> property specifies a code describing the job's extended status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d7474d1f-48f6-4515-8508-96eaf4e4281c">GroupBroadcastReceipts</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/d7474d1f-48f6-4515-8508-96eaf4e4281c">IFaxOutgoingJob::get_GroupBroadcastReceipts</a> property is a Boolean value that indicates whether to send an individual delivery receipt for each recipient of the broadcast or to send a summary receipt for all recipients.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/f19ee5c6-7d6f-48ab-82e1-52a6e11486a3">Id</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/f19ee5c6-7d6f-48ab-82e1-52a6e11486a3">IFaxOutgoingJob::get_Id</a> property is a null-terminated string that contains a unique identifier for the outbound fax job. You can use the identifier to retrieve the archived fax message after the job completes successfully.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9f6f3697-0334-4cc3-b737-4cd2069fee92">OriginalScheduledTime</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/9f6f3697-0334-4cc3-b737-4cd2069fee92">IFaxOutgoingJob::get_OriginalScheduledTime</a> property specifies the time that the fax job was originally scheduled for transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/bfb3087a-f791-4d44-887e-e19b05c5f5f1">Pages</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/bfb3087a-f791-4d44-887e-e19b05c5f5f1">IFaxOutgoingJob::get_Pages</a> property is a number that indicates the total number of pages in the outbound fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/0cf5d46f-0c26-4fa5-808e-13bdf1901964">Priority</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/0cf5d46f-0c26-4fa5-808e-13bdf1901964">IFaxOutgoingJob::get_Priority</a> property specifies the priority to use when sending the fax; for example, normal, low, or high priority.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/675fa0b8-758d-43b4-b493-ee8204f4b9c6">ReceiptType</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/675fa0b8-758d-43b4-b493-ee8204f4b9c6">IFaxOutgoingJob::get_ReceiptType</a> property is a value that specifies the type of delivery receipt to deliver when the fax message reaches a final state. The receipt type can be SMTP mail, a message box, or no receipt.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/cfc1d055-1bd1-4fbc-9b05-ca0a2807c5e5">Recipient</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/cfc1d055-1bd1-4fbc-9b05-ca0a2807c5e5">IFaxOutgoingJob::get_Recipient</a> property retrieves an interface to an object containing information about the recipient of the fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7c21eee8-3ac3-4d32-a5c7-4d1352c2e512">Retries</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/7c21eee8-3ac3-4d32-a5c7-4d1352c2e512">IFaxOutgoingJob::get_Retries</a> property is a value that indicates the number of times that the fax service attempted to transmit an outgoing fax after the initial transmission attempt failed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8c8d5681-ae27-4412-8182-d5ab702e6811">ScheduledTime</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/8c8d5681-ae27-4412-8182-d5ab702e6811">IFaxOutgoingJob::get_ScheduledTime</a> property indicates the time to submit the fax for processing to the fax service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/fbec5c4f-fb92-40d1-af9c-1faf7531cc2e">Sender</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/fbec5c4f-fb92-40d1-af9c-1faf7531cc2e">IFaxOutgoingJob::get_Sender</a> property retrieves an object containing information about the sender of the fax.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/17dc228a-8514-4ae4-af8e-f34177548748">Size</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/17dc228a-8514-4ae4-af8e-f34177548748">IFaxOutgoingJob::get_Size</a> property is a value that indicates the size of the TIFF Class F file associated with the outbound fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/90553615-ded2-4e4c-9411-a513fd682423">Status</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/90553615-ded2-4e4c-9411-a513fd682423">IFaxOutgoingJob::get_Status</a> property is a number that indicates the current status of an outbound fax job in the job queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/25109ef7-feae-40df-8087-5946ce87cfaa">Subject</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/25109ef7-feae-40df-8087-5946ce87cfaa">IFaxOutgoingJob::get_Subject</a> property is a null-terminated string that contains the contents of the subject field on the cover page of the fax.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e3dee57e-1f4d-4c78-8436-214d1778e5ff">SubmissionId</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/e3dee57e-1f4d-4c78-8436-214d1778e5ff">IFaxOutgoingJob::get_SubmissionId</a> property is a null-terminated string that contains the unique identifier assigned to the fax job during the submission process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/6a401fdb-2cf7-45f9-b56b-d7e72f5ec42d">SubmissionTime</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/6a401fdb-2cf7-45f9-b56b-d7e72f5ec42d">IFaxOutgoingJob::get_SubmissionTime</a> property indicates the time that the outbound fax job was submitted for processing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/aec02df6-e042-47ec-b008-d8af9108bccc">TransmissionEnd</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/aec02df6-e042-47ec-b008-d8af9108bccc">IFaxOutgoingJob::get_TransmissionEnd</a> property indicates the time that the outbound fax job completed transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/6ff12870-3f5e-4bac-b1f0-7a923e11f7d7">TransmissionStart</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/6ff12870-3f5e-4bac-b1f0-7a923e11f7d7">IFaxOutgoingJob::get_TransmissionStart</a> property indicates the time that the fax outbound job began transmitting. This property will have a value only after the transmission has started.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/fa4f6947-5261-475e-9ec0-c31c2a3b644f">TSID</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/fa4f6947-5261-475e-9ec0-c31c2a3b644f">IFaxOutgoingJob::get_TSID</a> property is a null-terminated string that contains the TSID associated with the fax outbound job.

</td>
</tr>
</table> 


## -remarks



A default implementation of <b>IFaxOutgoingJob</b> is provided as the <a href="https://msdn.microsoft.com/f9686d11-fd32-4eaf-ae93-399dacf028ac">FaxOutgoingJob</a> object.



