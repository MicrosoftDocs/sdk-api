---
UID: NN:faxcom.IFaxJob
title: IFaxJob
author: windows-sdk-content
description: The IFaxJob dual interface is used by a fax client application to access information for a fax job on a connected fax server. A FaxJobs object is a collection of FaxJob objects.
old-location: fax\_mfax_ifaxjob.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_75sy.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: IFaxJob, IFaxJob interface [Fax Service], IFaxJob interface [Fax Service],described, _mfax_ifaxjob, fax._mfax_ifaxjob, faxcom/IFaxJob
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: faxcom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Faxcom.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Faxcom.dll
api_name:
 - IFaxJob
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxJob interface


## -description


The <b>IFaxJob</b> dual interface is used by a fax client application to access information for a fax job on a connected fax server. A <a href="https://msdn.microsoft.com/7a8ad6e7-8db6-49ba-98de-da583907a54e">FaxJobs</a> object is a collection of <a href="https://msdn.microsoft.com/4c8376a4-dded-489e-a361-ce6edd0e17af">FaxJob</a> objects.

The IFaxJob interface includes the following methods.
			<ul>
<li>A method to modify the job queue status of a fax job.</li>
<li>A method to refresh FaxJob object information.</li>
<li>Property methods to retrieve individual property values associated with a FaxJob object retrieved by the IFaxJobs interface.</li>
</ul>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxJob</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFaxJob</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFaxJob</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ee1d91d5-cd99-4148-b665-8840ff0e069a">Refresh</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/ee1d91d5-cd99-4148-b665-8840ff0e069a">IFaxJob::Refresh</a> method updates <a href="https://msdn.microsoft.com/4c8376a4-dded-489e-a361-ce6edd0e17af">FaxJob</a> object information for the associated fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/91bec42d-c7ba-4c7c-941e-f08d6c4eefa0">SetStatus</a>
</td>
<td align="left" width="63%">
Call the <a href="https://msdn.microsoft.com/91bec42d-c7ba-4c7c-941e-f08d6c4eefa0">IFaxJob::SetStatus</a> method to pause, resume, cancel, or restart a specified fax job.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxJob</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/715ef2ac-75ba-465b-8498-adfa1aff6a6f">BillingCode</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/715ef2ac-75ba-465b-8498-adfa1aff6a6f">IFaxJob::get_BillingCode</a> property is a null-terminated string that contains an optional billing code that applies to the fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/2b5e3af4-7017-42a7-8b80-93dd3edd568b">DeviceStatus</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/2b5e3af4-7017-42a7-8b80-93dd3edd568b">IFaxJob::get_DeviceStatus</a> property is a null-terminated string that describes the status of the port associated with the fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/56b512bd-e075-431e-89ab-fbac072b07e3">DiscountSend</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/56b512bd-e075-431e-89ab-fbac072b07e3">IFaxJob::get_DiscountSend</a> property is a Boolean value that indicates whether the fax server will transmit the fax job during the discount rate period. The discount period applies only to outgoing fax transmissions. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/45ba0af1-25cc-4020-ae5c-355e318a63bf">DisplayName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/45ba0af1-25cc-4020-ae5c-355e318a63bf">IFaxJob::get_DisplayName</a> property is a null-terminated string that contains the user-friendly name to associate with the fax job.


</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/04af9c3e-5843-4e23-88f1-c685b87d6bcd">FaxNumber</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/04af9c3e-5843-4e23-88f1-c685b87d6bcd">IFaxJob::get_FaxNumber</a> property is a null-terminated string that contains the fax number to which the fax server will transmit the fax job. The <b>IFaxJob::get_FaxNumber</b> property applies only to outgoing fax transmissions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/81e6f533-1d92-4bb6-b69e-033e2ac0a0b4">JobId</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/81e6f533-1d92-4bb6-b69e-033e2ac0a0b4">IFaxJob::get_JobId</a> property is a number that uniquely identifies the specified fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/932ca9c4-3938-43bb-85b2-ba6b7f5877ad">PageCount</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/932ca9c4-3938-43bb-85b2-ba6b7f5877ad">IFaxJob::get_PageCount</a> property is a number that represents the total number of pages in a fax transmission. The <b>IFaxJob::get_PageCount</b> property applies only to outgoing fax transmissions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/79fac214-78cf-4271-8c79-aa75a1661a48">QueueStatus</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/79fac214-78cf-4271-8c79-aa75a1661a48">IFaxJob::get_QueueStatus</a> property is a null-terminated string that describes the job queue status of the fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d754b066-0f53-4b70-9384-6545b1b6cfdd">RecipientName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/d754b066-0f53-4b70-9384-6545b1b6cfdd">IFaxJob::get_RecipientName</a> property is a null-terminated string that contains the name of the recipient of the fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7e075905-f6cf-4d9e-bc3f-fdc7ce9a20c8">SenderCompany</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/7e075905-f6cf-4d9e-bc3f-fdc7ce9a20c8">IFaxJob::get_SenderCompany</a> property is a null-terminated string that contains the company name for the sender of the fax job. The <b>IFaxJob::get_SenderCompany</b> property applies only to outgoing fax transmissions.


</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/de66e25e-d20c-4fd5-a2ee-1e739d12edfd">SenderDept</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/de66e25e-d20c-4fd5-a2ee-1e739d12edfd">IFaxJob::get_SenderDept</a> property is a null-terminated string that contains the department identifier for the sender of the fax job. The <b>IFaxJob::get_SenderDept</b> property applies only to outgoing fax transmissions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/31a02244-4ea4-4231-aec3-3d699defcfc4">SenderName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/31a02244-4ea4-4231-aec3-3d699defcfc4">IFaxJob::get_SenderName</a> property is a null-terminated string that contains the name of the sender who initiated the fax job. The <b>IFaxJob::get_SenderName</b> property applies only to outgoing fax transmissions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/109b9be7-d00a-4a59-bab7-eec8060de14d">Tsid</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/109b9be7-d00a-4a59-bab7-eec8060de14d">IFaxJob::get_Tsid</a> property is a null-terminated string that contains the 
TSID) associated with the fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9c27ffde-ce52-4ef2-8f41-1a92884926bc">Type</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/9c27ffde-ce52-4ef2-8f41-1a92884926bc">IFaxJob::get_Type</a> property is a number that describes the type of fax job represented by the object. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/811ad121-1602-4829-bf6c-aef680eebe3f">UserName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/811ad121-1602-4829-bf6c-aef680eebe3f">IFaxJob::get_UserName</a> property is a null-terminated string that contains the name of the user who submitted the fax job to the job queue. The <b>IFaxJob::get_UserName</b> property applies only to outgoing fax transmissions.


</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
You should not implement this interface. The Microsoft standard implementation provides complete functionality. 

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Use the <b>IFaxJob</b> interface to access the job status for incoming and outgoing fax transmissions, and to pause, resume, cancel or restart a fax job. You can also use the interface to retrieve the properties of a <a href="https://msdn.microsoft.com/4c8376a4-dded-489e-a361-ce6edd0e17af">FaxJob</a> object.

A client application should not call the <a href="_com_CoCreateInstance">CoCreateInstance</a> function to retrieve an <b>IFaxJob</b> interface pointer. Instead, the application must perform the following steps to create an instance of a <a href="https://msdn.microsoft.com/4c8376a4-dded-489e-a361-ce6edd0e17af">FaxJob</a> object. 
				<ol>
<li>Call the <a href="_com_CoCreateInstance">CoCreateInstance</a> function to retrieve a pointer to an <a href="https://msdn.microsoft.com/f06b76b5-b6c2-47a0-ad08-7c1bf7b780bb">IFaxServer</a> interface.</li>
<li>Call the <a href="https://msdn.microsoft.com/12e71c4c-c4b5-4e6d-a1fa-b833d6a00ff8">IFaxServer::Connect</a> method to connect to an active fax server. </li>
<li>Call the <a href="https://msdn.microsoft.com/45b195f9-0ac9-4150-84cf-64049cc4053f">IFaxServer::GetJobs</a> method to create and initialize a <a href="https://msdn.microsoft.com/7a8ad6e7-8db6-49ba-98de-da583907a54e">FaxJobs</a> object for the connected fax server.</li>
<li>Call the <a href="https://msdn.microsoft.com/476d4381-30b4-4749-b1ea-fbd28ca8148d">IFaxJobs::get_Count</a> method and then the <a href="https://msdn.microsoft.com/1279c69b-42b0-4ce2-92e1-307d3d7999b4">IFaxJobs::get_Item</a> method to retrieve <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface pointers for each child <a href="https://msdn.microsoft.com/4c8376a4-dded-489e-a361-ce6edd0e17af">FaxJob</a> object. (You can also call the <a href="_com_IUnknown_QueryInterface">IUnknown::QueryInterface</a> method to retrieve an <b>IFaxJob</b> interface pointer.)</li>
<li>Use the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface pointer to call <b>IFaxJob</b> interface methods.</li>
<li>Call the <a href="https://msdn.microsoft.com/dccbb6b1-b889-4b73-a3d0-9c5ce6268f4a">IFaxServer::Disconnect</a> method to disconnect from the fax server.</li>
<li>Call the <a href="_com_IUnknown_Release">IUnknown::Release</a> method for each <a href="https://msdn.microsoft.com/4c8376a4-dded-489e-a361-ce6edd0e17af">FaxJob</a> object to allow the object to deallocate itself, and again to destroy the <a href="https://msdn.microsoft.com/c9e548c4-9381-4b7d-9a9d-55fbc59f198f">IFaxJobs</a> interface pointer.</li>
</ol>





## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

