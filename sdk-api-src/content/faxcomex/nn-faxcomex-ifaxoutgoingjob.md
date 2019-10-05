---
UID: NN:faxcomex.IFaxOutgoingJob
title: IFaxOutgoingJob (faxcomex.h)
author: windows-sdk-content
description: The IFaxOutgoingJob interface describes an object that is used by a fax client application to retrieve information about an outgoing fax job in a fax server's queue.
old-location: fax\_mfax_faxoutgoingjob_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_4mjm_cpp.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFaxOutgoingJob, IFaxOutgoingJob interface [Fax Service], IFaxOutgoingJob interface [Fax Service],described, _mfax_faxoutgoingjob_cpp, fax._mfax_faxoutgoingjob_cpp, faxcomex/IFaxOutgoingJob
ms.topic: interface
f1_keywords: 
 - "faxcomex/IFaxOutgoingJob"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxOutgoingJob interface


## -description


The <b>IFaxOutgoingJob</b> interface describes an object that is used by a fax client application to retrieve information about an outgoing fax job in a fax server's queue. The object also includes methods to cancel, pause, resume, or restart an outgoing fax job, and to copy the Tagged Image File Format Class F (TIFF Class F) file associated with an outbound fax job, to a file on the local computer.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxOutgoingJob</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxOutgoingJob</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-cancel-vb">Cancel</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-cancel-vb">IFaxOutgoingJob::Cancel</a> method cancels the outbound fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-copytiff-vb">CopyTiff</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-copytiff-vb">IFaxOutgoingJob::CopyTiff</a> method copies the TIFF Class F file associated with the outbound fax job, to a file on the local computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-pause-vb">Pause</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-pause-vb">IFaxOutgoingJob::Pause</a> method pauses the outbound fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-refresh-vb">Refresh</a>
</td>
<td align="left" width="63%">
The Refresh method refreshes <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob">FaxOutgoingJob</a> object information from the fax server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-restart-vb">Restart</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-restart-vb">IFaxOutgoingJob::Restart</a> method restarts the failed outbound fax job. For example, if the fax job has exceeded the number of retries, <b>IFaxOutgoingJob::Restart</b> will restart the fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-resume-vb">Resume</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-resume-vb">IFaxOutgoingJob::Resume</a> method resumes the paused outbound fax job.

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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-availableoperations-vb">AvailableOperations</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-availableoperations-vb">IFaxOutgoingJob::get_AvailableOperations</a> property indicates the combination of valid operations that you can perform on the fax job, given its current status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-csid-vb">CSID</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-csid-vb">IFaxOutgoingJob::get_CSID</a> property is a null-terminated string that contains the CSID associated with the fax outbound job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-currentpage-vb">CurrentPage</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-currentpage-vb">IFaxOutgoingJob::get_CurrentPage</a> property is a number that identifies the page that the fax service is actively transmitting on an outbound fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-deviceid-vb">DeviceId</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-deviceid-vb">IFaxOutgoingJob::get_DeviceId</a> property indicates the device ID of the device transmitting the outbound fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-documentname-vb">DocumentName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-documentname-vb">IFaxOutgoingJob::get_DocumentName</a> property is a null-terminated string that contains the user-friendly name to display for the fax document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-extendedstatus-vb">ExtendedStatus</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-extendedstatus-vb">IFaxOutgoingJob::get_ExtendedStatus</a> property is a null-terminated string that describes the job's extended status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-extendedstatuscode-vb">ExtendedStatusCode</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-extendedstatuscode-vb">IFaxOutgoingJob::get_ExtendedStatusCode</a> property specifies a code describing the job's extended status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-groupbroadcastreceipts-vb">GroupBroadcastReceipts</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-groupbroadcastreceipts-vb">IFaxOutgoingJob::get_GroupBroadcastReceipts</a> property is a Boolean value that indicates whether to send an individual delivery receipt for each recipient of the broadcast or to send a summary receipt for all recipients.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-id-vb">Id</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-id-vb">IFaxOutgoingJob::get_Id</a> property is a null-terminated string that contains a unique identifier for the outbound fax job. You can use the identifier to retrieve the archived fax message after the job completes successfully.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-originalscheduledtime-vb">OriginalScheduledTime</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-originalscheduledtime-vb">IFaxOutgoingJob::get_OriginalScheduledTime</a> property specifies the time that the fax job was originally scheduled for transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-pages-vb">Pages</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-pages-vb">IFaxOutgoingJob::get_Pages</a> property is a number that indicates the total number of pages in the outbound fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-priority-vb">Priority</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-priority-vb">IFaxOutgoingJob::get_Priority</a> property specifies the priority to use when sending the fax; for example, normal, low, or high priority.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-receipttype-vb">ReceiptType</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-receipttype-vb">IFaxOutgoingJob::get_ReceiptType</a> property is a value that specifies the type of delivery receipt to deliver when the fax message reaches a final state. The receipt type can be SMTP mail, a message box, or no receipt.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxoutgoingjob-get_recipient">Recipient</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxoutgoingjob-get_recipient">IFaxOutgoingJob::get_Recipient</a> property retrieves an interface to an object containing information about the recipient of the fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-retries-vb">Retries</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-retries-vb">IFaxOutgoingJob::get_Retries</a> property is a value that indicates the number of times that the fax service attempted to transmit an outgoing fax after the initial transmission attempt failed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-scheduledtime-vb">ScheduledTime</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-scheduledtime-vb">IFaxOutgoingJob::get_ScheduledTime</a> property indicates the time to submit the fax for processing to the fax service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxoutgoingjob-get_sender">Sender</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxoutgoingjob-get_sender">IFaxOutgoingJob::get_Sender</a> property retrieves an object containing information about the sender of the fax.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-size-vb">Size</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-size-vb">IFaxOutgoingJob::get_Size</a> property is a value that indicates the size of the TIFF Class F file associated with the outbound fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-status-vb">Status</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-status-vb">IFaxOutgoingJob::get_Status</a> property is a number that indicates the current status of an outbound fax job in the job queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-subject-vb">Subject</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-subject-vb">IFaxOutgoingJob::get_Subject</a> property is a null-terminated string that contains the contents of the subject field on the cover page of the fax.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-submissionid-vb">SubmissionId</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-submissionid-vb">IFaxOutgoingJob::get_SubmissionId</a> property is a null-terminated string that contains the unique identifier assigned to the fax job during the submission process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-submissiontime-vb">SubmissionTime</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-submissiontime-vb">IFaxOutgoingJob::get_SubmissionTime</a> property indicates the time that the outbound fax job was submitted for processing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-transmissionend-vb">TransmissionEnd</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-transmissionend-vb">IFaxOutgoingJob::get_TransmissionEnd</a> property indicates the time that the outbound fax job completed transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-transmissionstart-vb">TransmissionStart</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-transmissionstart-vb">IFaxOutgoingJob::get_TransmissionStart</a> property indicates the time that the fax outbound job began transmitting. This property will have a value only after the transmission has started.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-tsid-vb">TSID</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-tsid-vb">IFaxOutgoingJob::get_TSID</a> property is a null-terminated string that contains the TSID associated with the fax outbound job.

</td>
</tr>
</table> 


## -remarks



A default implementation of <b>IFaxOutgoingJob</b> is provided as the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob">FaxOutgoingJob</a> object.



