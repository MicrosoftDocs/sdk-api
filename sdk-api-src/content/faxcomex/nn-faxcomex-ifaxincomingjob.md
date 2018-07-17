---
UID: NN:faxcomex.IFaxIncomingJob
title: IFaxIncomingJob
author: windows-sdk-content
description: The IFaxIncomingJob interface is used by a fax client application to retrieve information about an incoming fax job in a fax server's queue.
old-location: fax\_mfax_faxincomingjob_cpp.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_1r4y_cpp.htm
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: IFaxIncomingJob, IFaxIncomingJob interface [Fax Service], IFaxIncomingJob interface [Fax Service],described, _mfax_faxincomingjob_cpp, fax._mfax_faxincomingjob_cpp, faxcomex/IFaxIncomingJob
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
 - IFaxIncomingJob
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxIncomingJob interface


## -description


The <b>IFaxIncomingJob</b> interface is used by a fax client application to retrieve information about an incoming fax job in a fax server's queue. The interface also includes methods to cancel an incoming fax job and to copy the Tagged Image File Format Class F (TIFF Class F) file associated with an inbound fax job to a file on the local computer.

The <b>IFaxIncomingJob</b> interface is accessed through the <a href="https://msdn.microsoft.com/library/ms684964(v=VS.85).aspx">IFaxIncomingJobs</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxIncomingJob</b> interface inherits from the <a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IFaxIncomingJob</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406716">Cancel</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/library/windows/hardware/hh406716">Cancel</a> method cancels the incoming fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/ms684597(v=VS.85).aspx">CopyTiff</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/library/ms684597(v=VS.85).aspx">CopyTiff</a> method copies the TIFF Class F file associated with the inbound fax job to a file on the local computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/ms684594(v=VS.85).aspx">get_AvailableOperations</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/library/ms684594(v=VS.85).aspx">AvailableOperations</a> property of a <a href="https://msdn.microsoft.com/library/ms684876(v=VS.85).aspx">FaxIncomingJob</a> object. The <b>AvailableOperations</b> property indicates the combination of valid operations that you can perform on the fax job given its current status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/ms686035(v=VS.85).aspx">get_ExtendedStatusCode</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/library/ms686035(v=VS.85).aspx">ExtendedStatusCode</a> property of a <a href="https://msdn.microsoft.com/library/ms684876(v=VS.85).aspx">FaxIncomingJob</a> object. The <b>ExtendedStatusCode</b> property specifies a code describing the job's extended status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/ms687472(v=VS.85).aspx">get_JobType</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/library/ms687472(v=VS.85).aspx">JobType</a> property of a <a href="https://msdn.microsoft.com/library/ms684876(v=VS.85).aspx">FaxIncomingJob</a> object. The <a href="https://msdn.microsoft.com/library/ms687471(v=VS.85).aspx">JobType</a> property describes the type of fax job; for example, the job can be a receive job, a send job, or a routing job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/ms684830(v=VS.85).aspx">get_Status</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> property of a <a href="https://msdn.microsoft.com/library/ms684876(v=VS.85).aspx">FaxIncomingJob</a> object. The <b>Status</b> property is a number that indicates the current status of an inbound fax job in the job queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ac2c2265-5a47-4fcb-89bb-ab80decdcce2">Refresh</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/ac2c2265-5a47-4fcb-89bb-ab80decdcce2">Refresh</a> method refreshes <a href="https://msdn.microsoft.com/library/ms684876(v=VS.85).aspx">FaxIncomingJob</a> object information from the fax server.

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

<a href="https://msdn.microsoft.com/library/ms684572(v=VS.85).aspx">CallerId</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/library/ms684572(v=VS.85).aspx">CallerId</a> property is a string that identifies the calling device that sent the inbound fax job.

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
The <a href="https://msdn.microsoft.com/library/windows/hardware/dn922691">CSID</a> property is a null-terminated string that contains the CSID for the job.

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

<a href="https://msdn.microsoft.com/library/windows/hardware/dn895599">Id</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/library/windows/hardware/dn895599">Id</a> property is a null-terminated string that contains a unique ID for the inbound fax job.

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

<a href="https://msdn.microsoft.com/library/windows/hardware/dn915850">Size</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/library/windows/hardware/dn915850">Size</a> property is a value that indicates the size of the TIFF Class F file associated with the inbound fax job.

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

<a href="https://msdn.microsoft.com/library/windows/hardware/dn997387">TSID</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/library/windows/hardware/dn997387">TSID</a> property is a null-terminated string that contains the TSID associated with the fax inbound job.

</td>
</tr>
</table> 


## -remarks



To create a <b>FaxIncomingJob</b> object in C++, call the <a href="https://msdn.microsoft.com/library/ms686185(v=VS.85).aspx">IFaxIncomingJobs::get_Item</a> method.




## -see-also




<a href="https://msdn.microsoft.com/library/ms684876(v=VS.85).aspx">FaxIncomingJob</a>



<a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/library/ms684964(v=VS.85).aspx">IFaxIncomingJobs</a>
 

 

