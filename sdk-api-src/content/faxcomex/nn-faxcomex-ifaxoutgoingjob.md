---
UID: NN:faxcomex.IFaxOutgoingJob
title: IFaxOutgoingJob
author: windows-sdk-content
description: The IFaxOutgoingJob interface describes an object that is used by a fax client application to retrieve information about an outgoing fax job in a fax server's queue.
old-location: fax\_mfax_faxoutgoingjob_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_4mjm_cpp.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxOutgoingJob</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IFaxOutgoingJob</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/ms690052(v=VS.85).aspx">Cancel</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms690052(v=VS.85).aspx">IFaxOutgoingJob::Cancel</a> method cancels the outbound fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms690130(v=VS.85).aspx">CopyTiff</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms690130(v=VS.85).aspx">IFaxOutgoingJob::CopyTiff</a> method copies the TIFF Class F file associated with the outbound fax job, to a file on the local computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms689601(v=VS.85).aspx">Pause</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms689601(v=VS.85).aspx">IFaxOutgoingJob::Pause</a> method pauses the outbound fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms688498(v=VS.85).aspx">Refresh</a>
</td>
<td align="left" width="63%">
The Refresh method refreshes <a href="https://msdn.microsoft.com/en-us/library/ms689115(v=VS.85).aspx">FaxOutgoingJob</a> object information from the fax server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms690070(v=VS.85).aspx">Restart</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms690070(v=VS.85).aspx">IFaxOutgoingJob::Restart</a> method restarts the failed outbound fax job. For example, if the fax job has exceeded the number of retries, <b>IFaxOutgoingJob::Restart</b> will restart the fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms689539(v=VS.85).aspx">Resume</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms689539(v=VS.85).aspx">IFaxOutgoingJob::Resume</a> method resumes the paused outbound fax job.

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

<a href="https://msdn.microsoft.com/en-us/library/ms690257(v=VS.85).aspx">AvailableOperations</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms690257(v=VS.85).aspx">IFaxOutgoingJob::get_AvailableOperations</a> property indicates the combination of valid operations that you can perform on the fax job, given its current status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms689548(v=VS.85).aspx">CSID</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms689548(v=VS.85).aspx">IFaxOutgoingJob::get_CSID</a> property is a null-terminated string that contains the CSID associated with the fax outbound job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms688621(v=VS.85).aspx">CurrentPage</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms688621(v=VS.85).aspx">IFaxOutgoingJob::get_CurrentPage</a> property is a number that identifies the page that the fax service is actively transmitting on an outbound fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms689123(v=VS.85).aspx">DeviceId</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms689123(v=VS.85).aspx">IFaxOutgoingJob::get_DeviceId</a> property indicates the device ID of the device transmitting the outbound fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms689177(v=VS.85).aspx">DocumentName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms689177(v=VS.85).aspx">IFaxOutgoingJob::get_DocumentName</a> property is a null-terminated string that contains the user-friendly name to display for the fax document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms688590(v=VS.85).aspx">ExtendedStatus</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms688590(v=VS.85).aspx">IFaxOutgoingJob::get_ExtendedStatus</a> property is a null-terminated string that describes the job's extended status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms687986(v=VS.85).aspx">ExtendedStatusCode</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms687986(v=VS.85).aspx">IFaxOutgoingJob::get_ExtendedStatusCode</a> property specifies a code describing the job's extended status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms689107(v=VS.85).aspx">GroupBroadcastReceipts</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms689107(v=VS.85).aspx">IFaxOutgoingJob::get_GroupBroadcastReceipts</a> property is a Boolean value that indicates whether to send an individual delivery receipt for each recipient of the broadcast or to send a summary receipt for all recipients.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms689209(v=VS.85).aspx">Id</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms689209(v=VS.85).aspx">IFaxOutgoingJob::get_Id</a> property is a null-terminated string that contains a unique identifier for the outbound fax job. You can use the identifier to retrieve the archived fax message after the job completes successfully.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms690221(v=VS.85).aspx">OriginalScheduledTime</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms690221(v=VS.85).aspx">IFaxOutgoingJob::get_OriginalScheduledTime</a> property specifies the time that the fax job was originally scheduled for transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms689528(v=VS.85).aspx">Pages</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms689528(v=VS.85).aspx">IFaxOutgoingJob::get_Pages</a> property is a number that indicates the total number of pages in the outbound fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms689543(v=VS.85).aspx">Priority</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms689543(v=VS.85).aspx">IFaxOutgoingJob::get_Priority</a> property specifies the priority to use when sending the fax; for example, normal, low, or high priority.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms689599(v=VS.85).aspx">ReceiptType</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms689599(v=VS.85).aspx">IFaxOutgoingJob::get_ReceiptType</a> property is a value that specifies the type of delivery receipt to deliver when the fax message reaches a final state. The receipt type can be SMTP mail, a message box, or no receipt.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms689580(v=VS.85).aspx">Recipient</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms689580(v=VS.85).aspx">IFaxOutgoingJob::get_Recipient</a> property retrieves an interface to an object containing information about the recipient of the fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms689583(v=VS.85).aspx">Retries</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms689583(v=VS.85).aspx">IFaxOutgoingJob::get_Retries</a> property is a value that indicates the number of times that the fax service attempted to transmit an outgoing fax after the initial transmission attempt failed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms688077(v=VS.85).aspx">ScheduledTime</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms688077(v=VS.85).aspx">IFaxOutgoingJob::get_ScheduledTime</a> property indicates the time to submit the fax for processing to the fax service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms687547(v=VS.85).aspx">Sender</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms687547(v=VS.85).aspx">IFaxOutgoingJob::get_Sender</a> property retrieves an object containing information about the sender of the fax.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms689187(v=VS.85).aspx">Size</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms689187(v=VS.85).aspx">IFaxOutgoingJob::get_Size</a> property is a value that indicates the size of the TIFF Class F file associated with the outbound fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms688565(v=VS.85).aspx">Status</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms688565(v=VS.85).aspx">IFaxOutgoingJob::get_Status</a> property is a number that indicates the current status of an outbound fax job in the job queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms687530(v=VS.85).aspx">Subject</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms687530(v=VS.85).aspx">IFaxOutgoingJob::get_Subject</a> property is a null-terminated string that contains the contents of the subject field on the cover page of the fax.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms690201(v=VS.85).aspx">SubmissionId</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms690201(v=VS.85).aspx">IFaxOutgoingJob::get_SubmissionId</a> property is a null-terminated string that contains the unique identifier assigned to the fax job during the submission process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms688457(v=VS.85).aspx">SubmissionTime</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms688457(v=VS.85).aspx">IFaxOutgoingJob::get_SubmissionTime</a> property indicates the time that the outbound fax job was submitted for processing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms689136(v=VS.85).aspx">TransmissionEnd</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms689136(v=VS.85).aspx">IFaxOutgoingJob::get_TransmissionEnd</a> property indicates the time that the outbound fax job completed transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms688396(v=VS.85).aspx">TransmissionStart</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms688396(v=VS.85).aspx">IFaxOutgoingJob::get_TransmissionStart</a> property indicates the time that the fax outbound job began transmitting. This property will have a value only after the transmission has started.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms688379(v=VS.85).aspx">TSID</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms688379(v=VS.85).aspx">IFaxOutgoingJob::get_TSID</a> property is a null-terminated string that contains the TSID associated with the fax outbound job.

</td>
</tr>
</table> 


## -remarks



A default implementation of <b>IFaxOutgoingJob</b> is provided as the <a href="https://msdn.microsoft.com/en-us/library/ms689115(v=VS.85).aspx">FaxOutgoingJob</a> object.



