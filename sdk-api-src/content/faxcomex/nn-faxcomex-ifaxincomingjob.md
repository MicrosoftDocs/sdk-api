---
UID: NN:faxcomex.IFaxIncomingJob
title: IFaxIncomingJob (faxcomex.h)
author: windows-sdk-content
description: The IFaxIncomingJob interface is used by a fax client application to retrieve information about an incoming fax job in a fax server's queue.
old-location: fax\_mfax_faxincomingjob_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_1r4y_cpp.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFaxIncomingJob, IFaxIncomingJob interface [Fax Service], IFaxIncomingJob interface [Fax Service],described, _mfax_faxincomingjob_cpp, fax._mfax_faxincomingjob_cpp, faxcomex/IFaxIncomingJob
ms.topic: interface
f1_keywords: 
 - "faxcomex/IFaxIncomingJob"
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
 - IFaxIncomingJob
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxIncomingJob interface


## -description


The <b>IFaxIncomingJob</b> interface is used by a fax client application to retrieve information about an incoming fax job in a fax server's queue. The interface also includes methods to cancel an incoming fax job and to copy the Tagged Image File Format Class F (TIFF Class F) file associated with an inbound fax job to a file on the local computer.

The <b>IFaxIncomingJob</b> interface is accessed through the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingjobs">IFaxIncomingJobs</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxIncomingJob</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxIncomingJob</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFaxIncomingJob</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingjob-cancel-vb">Cancel</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingjob-cancel-vb">Cancel</a> method cancels the incoming fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingjob-copytiff-vb">CopyTiff</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingjob-copytiff-vb">CopyTiff</a> method copies the TIFF Class F file associated with the inbound fax job to a file on the local computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxincomingjob-get_availableoperations">get_AvailableOperations</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxincomingjob-get_availableoperations">AvailableOperations</a> property of a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingjob">FaxIncomingJob</a> object. The <b>AvailableOperations</b> property indicates the combination of valid operations that you can perform on the fax job given its current status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxincomingjob-get_extendedstatuscode">get_ExtendedStatusCode</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxincomingjob-get_extendedstatuscode">ExtendedStatusCode</a> property of a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingjob">FaxIncomingJob</a> object. The <b>ExtendedStatusCode</b> property specifies a code describing the job's extended status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxincomingjob-get_jobtype">get_JobType</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxincomingjob-get_jobtype">JobType</a> property of a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingjob">FaxIncomingJob</a> object. The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingjob-jobtype">JobType</a> property describes the type of fax job; for example, the job can be a receive job, a send job, or a routing job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxincomingjob-get_status">get_Status</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxincomingjob-get_status">Status</a> property of a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingjob">FaxIncomingJob</a> object. The <b>Status</b> property is a number that indicates the current status of an inbound fax job in the job queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingjob-refresh-vb">Refresh</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingjob-refresh-vb">Refresh</a> method refreshes <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingjob">FaxIncomingJob</a> object information from the fax server.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxIncomingJob</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingjob-callerid-vb">CallerId</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingjob-callerid-vb">CallerId</a> property is a string that identifies the calling device that sent the inbound fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingjob-csid-vb">CSID</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingjob-csid-vb">CSID</a> property is a null-terminated string that contains the CSID for the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingjob-currentpage-vb">CurrentPage</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingjob-currentpage-vb">CurrentPage</a> property is a number that identifies the page that the fax service is actively receiving on an inbound fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingjob-deviceid-vb">DeviceId</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingjob-deviceid-vb">DeviceId</a> property indicates the device ID of the device receiving the inbound fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingjob-extendedstatus-vb">ExtendedStatus</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingjob-extendedstatus-vb">ExtendedStatus</a> property is a null-terminated string that describes the job's extended status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingjob-id-vb">Id</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingjob-id-vb">Id</a> property is a null-terminated string that contains a unique ID for the inbound fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingjob-retries-vb">Retries</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingjob-retries-vb">Retries</a> property is a value that indicates the number of times the fax service attempted to route an incoming fax when the initial routing attempt failed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingjob-routinginformation-vb">RoutingInformation</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingjob-routinginformation-vb">RoutingInformation</a> property is a null-terminated string that specifies routing information for the inbound fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingjob-size-vb">Size</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingjob-size-vb">Size</a> property is a value that indicates the size of the TIFF Class F file associated with the inbound fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingjob-transmissionend-vb">TransmissionEnd</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingjob-transmissionend-vb">TransmissionEnd</a> property indicates the time at which the inbound fax job completed transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingjob-transmissionstart-vb">TransmissionStart</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingjob-transmissionstart-vb">TransmissionStart</a> property indicates the time that the fax inbound job began transmitting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingjob-tsid-vb">TSID</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingjob-tsid-vb">TSID</a> property is a null-terminated string that contains the TSID associated with the fax inbound job.

</td>
</tr>
</table> 


## -remarks



To create a <b>FaxIncomingJob</b> object in C++, call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxincomingjobs-get_item">IFaxIncomingJobs::get_Item</a> method.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingjob">FaxIncomingJob</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingjobs">IFaxIncomingJobs</a>
 

 

