---
UID: NN:faxcomex.IFaxIncomingJob
title: IFaxIncomingJob
author: windows-sdk-content
description: The IFaxIncomingJob interface is used by a fax client application to retrieve information about an incoming fax job in a fax server's queue.
old-location: fax\_mfax_faxincomingjob_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_1r4y_cpp.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IFaxIncomingJob, IFaxIncomingJob interface [Fax Service], IFaxIncomingJob interface [Fax Service],described, _mfax_faxincomingjob_cpp, fax._mfax_faxincomingjob_cpp, faxcomex/IFaxIncomingJob
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
 - IFaxIncomingJob
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxIncomingJob interface


## -description


The <b>IFaxIncomingJob</b> interface is used by a fax client application to retrieve information about an incoming fax job in a fax server's queue. The interface also includes methods to cancel an incoming fax job and to copy the Tagged Image File Format Class F (TIFF Class F) file associated with an inbound fax job to a file on the local computer.

The <b>IFaxIncomingJob</b> interface is accessed through the <a href="https://msdn.microsoft.com/970a6047-4c85-404d-ad7e-39703f09f856">IFaxIncomingJobs</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxIncomingJob</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFaxIncomingJob</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/56c356cc-2630-40fc-b1fc-2571b2b16d7f">Cancel</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/56c356cc-2630-40fc-b1fc-2571b2b16d7f">Cancel</a> method cancels the incoming fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/56c67efa-e38a-403e-bb46-30379dfb4926">CopyTiff</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/56c67efa-e38a-403e-bb46-30379dfb4926">CopyTiff</a> method copies the TIFF Class F file associated with the inbound fax job to a file on the local computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1114284f-3150-421e-9171-dcbd572a9c45">get_AvailableOperations</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/1114284f-3150-421e-9171-dcbd572a9c45">AvailableOperations</a> property of a <a href="https://msdn.microsoft.com/ef93899d-e797-4f07-bede-0860b695b32b">FaxIncomingJob</a> object. The <b>AvailableOperations</b> property indicates the combination of valid operations that you can perform on the fax job given its current status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/005271e4-7ba6-4321-8575-28692015d780">get_ExtendedStatusCode</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/005271e4-7ba6-4321-8575-28692015d780">ExtendedStatusCode</a> property of a <a href="https://msdn.microsoft.com/ef93899d-e797-4f07-bede-0860b695b32b">FaxIncomingJob</a> object. The <b>ExtendedStatusCode</b> property specifies a code describing the job's extended status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5c6f3a10-b665-48a5-b4da-8beed66079f3">get_JobType</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/5c6f3a10-b665-48a5-b4da-8beed66079f3">JobType</a> property of a <a href="https://msdn.microsoft.com/ef93899d-e797-4f07-bede-0860b695b32b">FaxIncomingJob</a> object. The <a href="https://msdn.microsoft.com/53768e23-f93c-4fa7-b16e-23292f5a4380">JobType</a> property describes the type of fax job; for example, the job can be a receive job, a send job, or a routing job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fdcb2c7c-f2ca-402d-9a76-b6231142d7f1">get_Status</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/fdcb2c7c-f2ca-402d-9a76-b6231142d7f1">Status</a> property of a <a href="https://msdn.microsoft.com/ef93899d-e797-4f07-bede-0860b695b32b">FaxIncomingJob</a> object. The <b>Status</b> property is a number that indicates the current status of an inbound fax job in the job queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ac2c2265-5a47-4fcb-89bb-ab80decdcce2">Refresh</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/ac2c2265-5a47-4fcb-89bb-ab80decdcce2">Refresh</a> method refreshes <a href="https://msdn.microsoft.com/ef93899d-e797-4f07-bede-0860b695b32b">FaxIncomingJob</a> object information from the fax server.

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

<a href="https://msdn.microsoft.com/c1192439-7b74-40e9-9de1-5d7842d55921">CallerId</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/c1192439-7b74-40e9-9de1-5d7842d55921">CallerId</a> property is a string that identifies the calling device that sent the inbound fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/b7671766-4abb-460a-9f81-153e7e2dc9c9">CSID</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/b7671766-4abb-460a-9f81-153e7e2dc9c9">CSID</a> property is a null-terminated string that contains the CSID for the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/a6fa5376-15cb-4ac7-a7e4-ced0ff0a70e8">CurrentPage</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/a6fa5376-15cb-4ac7-a7e4-ced0ff0a70e8">CurrentPage</a> property is a number that identifies the page that the fax service is actively receiving on an inbound fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/65f47403-97fa-411d-b6f3-fbbc7c55cabf">DeviceId</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/65f47403-97fa-411d-b6f3-fbbc7c55cabf">DeviceId</a> property indicates the device ID of the device receiving the inbound fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/4280eb52-c5fa-4e06-8395-b7039d27eccc">ExtendedStatus</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/4280eb52-c5fa-4e06-8395-b7039d27eccc">ExtendedStatus</a> property is a null-terminated string that describes the job's extended status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9746a21c-9187-4ba7-9124-24ca943798f5">Id</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/9746a21c-9187-4ba7-9124-24ca943798f5">Id</a> property is a null-terminated string that contains a unique ID for the inbound fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/c45950c5-2910-4367-bee7-e813851a6f9a">Retries</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/c45950c5-2910-4367-bee7-e813851a6f9a">Retries</a> property is a value that indicates the number of times the fax service attempted to route an incoming fax when the initial routing attempt failed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/b9b7c8fc-cb72-42c6-8ab9-e07f3332a40c">RoutingInformation</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/b9b7c8fc-cb72-42c6-8ab9-e07f3332a40c">RoutingInformation</a> property is a null-terminated string that specifies routing information for the inbound fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d460834f-b38f-43ee-8fa2-21455b08819b">Size</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/d460834f-b38f-43ee-8fa2-21455b08819b">Size</a> property is a value that indicates the size of the TIFF Class F file associated with the inbound fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/313225b4-f515-4f1b-bb20-cd2b2ebf1996">TransmissionEnd</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/313225b4-f515-4f1b-bb20-cd2b2ebf1996">TransmissionEnd</a> property indicates the time at which the inbound fax job completed transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/49425bf3-28ac-4976-ad8e-b704e9d8dcb7">TransmissionStart</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/49425bf3-28ac-4976-ad8e-b704e9d8dcb7">TransmissionStart</a> property indicates the time that the fax inbound job began transmitting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/b7998949-5557-4df8-9fb4-f1170c13d201">TSID</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/b7998949-5557-4df8-9fb4-f1170c13d201">TSID</a> property is a null-terminated string that contains the TSID associated with the fax inbound job.

</td>
</tr>
</table> 


## -remarks



To create a <b>FaxIncomingJob</b> object in C++, call the <a href="https://msdn.microsoft.com/e6d1dbb5-7019-4a84-8118-4aff00a87b1b">IFaxIncomingJobs::get_Item</a> method.




## -see-also




<a href="https://msdn.microsoft.com/ef93899d-e797-4f07-bede-0860b695b32b">FaxIncomingJob</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/970a6047-4c85-404d-ad7e-39703f09f856">IFaxIncomingJobs</a>
 

 

