---
UID: NN:faxcom.IFaxJob
title: IFaxJob
author: windows-sdk-content
description: The IFaxJob dual interface is used by a fax client application to access information for a fax job on a connected fax server. A FaxJobs object is a collection of FaxJob objects.
old-location: fax\_mfax_ifaxjob.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_75sy.htm
ms.author: windowssdkdev
ms.date: 11/05/2018
ms.keywords: IFaxJob, IFaxJob interface [Fax Service], IFaxJob interface [Fax Service],described, _mfax_ifaxjob, fax._mfax_ifaxjob, faxcom/IFaxJob
ms.prod: windows
ms.technology: windows-sdk
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


The <b>IFaxJob</b> dual interface is used by a fax client application to access information for a fax job on a connected fax server. A <a href="https://msdn.microsoft.com/en-us/library/ms692796(v=VS.85).aspx">FaxJobs</a> object is a collection of <a href="https://msdn.microsoft.com/en-us/library/ms692342(v=VS.85).aspx">FaxJob</a> objects.

The IFaxJob interface includes the following methods.
			<ul>
<li>A method to modify the job queue status of a fax job.</li>
<li>A method to refresh FaxJob object information.</li>
<li>Property methods to retrieve individual property values associated with a FaxJob object retrieved by the IFaxJobs interface.</li>
</ul>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxJob</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IFaxJob</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/ms692320(v=VS.85).aspx">Refresh</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms692320(v=VS.85).aspx">IFaxJob::Refresh</a> method updates <a href="https://msdn.microsoft.com/en-us/library/ms692342(v=VS.85).aspx">FaxJob</a> object information for the associated fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms691414(v=VS.85).aspx">SetStatus</a>
</td>
<td align="left" width="63%">
Call the <a href="https://msdn.microsoft.com/en-us/library/ms691414(v=VS.85).aspx">IFaxJob::SetStatus</a> method to pause, resume, cancel, or restart a specified fax job.

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

<a href="https://msdn.microsoft.com/en-us/library/ms691346(v=VS.85).aspx">BillingCode</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms691346(v=VS.85).aspx">IFaxJob::get_BillingCode</a> property is a null-terminated string that contains an optional billing code that applies to the fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms690885(v=VS.85).aspx">DeviceStatus</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms690885(v=VS.85).aspx">IFaxJob::get_DeviceStatus</a> property is a null-terminated string that describes the status of the port associated with the fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms692784(v=VS.85).aspx">DiscountSend</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms692784(v=VS.85).aspx">IFaxJob::get_DiscountSend</a> property is a Boolean value that indicates whether the fax server will transmit the fax job during the discount rate period. The discount period applies only to outgoing fax transmissions. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms692370(v=VS.85).aspx">DisplayName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms692370(v=VS.85).aspx">IFaxJob::get_DisplayName</a> property is a null-terminated string that contains the user-friendly name to associate with the fax job.


</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms691808(v=VS.85).aspx">FaxNumber</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms691808(v=VS.85).aspx">IFaxJob::get_FaxNumber</a> property is a null-terminated string that contains the fax number to which the fax server will transmit the fax job. The <b>IFaxJob::get_FaxNumber</b> property applies only to outgoing fax transmissions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms690870(v=VS.85).aspx">JobId</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms690870(v=VS.85).aspx">IFaxJob::get_JobId</a> property is a number that uniquely identifies the specified fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms690850(v=VS.85).aspx">PageCount</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms690850(v=VS.85).aspx">IFaxJob::get_PageCount</a> property is a number that represents the total number of pages in a fax transmission. The <b>IFaxJob::get_PageCount</b> property applies only to outgoing fax transmissions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms692790(v=VS.85).aspx">QueueStatus</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms692790(v=VS.85).aspx">IFaxJob::get_QueueStatus</a> property is a null-terminated string that describes the job queue status of the fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms691934(v=VS.85).aspx">RecipientName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms691934(v=VS.85).aspx">IFaxJob::get_RecipientName</a> property is a null-terminated string that contains the name of the recipient of the fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms692349(v=VS.85).aspx">SenderCompany</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms692349(v=VS.85).aspx">IFaxJob::get_SenderCompany</a> property is a null-terminated string that contains the company name for the sender of the fax job. The <b>IFaxJob::get_SenderCompany</b> property applies only to outgoing fax transmissions.


</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms692305(v=VS.85).aspx">SenderDept</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms692305(v=VS.85).aspx">IFaxJob::get_SenderDept</a> property is a null-terminated string that contains the department identifier for the sender of the fax job. The <b>IFaxJob::get_SenderDept</b> property applies only to outgoing fax transmissions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms691367(v=VS.85).aspx">SenderName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms691367(v=VS.85).aspx">IFaxJob::get_SenderName</a> property is a null-terminated string that contains the name of the sender who initiated the fax job. The <b>IFaxJob::get_SenderName</b> property applies only to outgoing fax transmissions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms691869(v=VS.85).aspx">Tsid</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms691869(v=VS.85).aspx">IFaxJob::get_Tsid</a> property is a null-terminated string that contains the 
TSID) associated with the fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms691914(v=VS.85).aspx">Type</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms691914(v=VS.85).aspx">IFaxJob::get_Type</a> property is a number that describes the type of fax job represented by the object. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms691960(v=VS.85).aspx">UserName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms691960(v=VS.85).aspx">IFaxJob::get_UserName</a> property is a null-terminated string that contains the name of the user who submitted the fax job to the job queue. The <b>IFaxJob::get_UserName</b> property applies only to outgoing fax transmissions.


</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
You should not implement this interface. The Microsoft standard implementation provides complete functionality. 

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Use the <b>IFaxJob</b> interface to access the job status for incoming and outgoing fax transmissions, and to pause, resume, cancel or restart a fax job. You can also use the interface to retrieve the properties of a <a href="https://msdn.microsoft.com/en-us/library/ms692342(v=VS.85).aspx">FaxJob</a> object.

A client application should not call the <a href="https://msdn.microsoft.com/en-us/library/ms686615(v=VS.85).aspx">CoCreateInstance</a> function to retrieve an <b>IFaxJob</b> interface pointer. Instead, the application must perform the following steps to create an instance of a <a href="https://msdn.microsoft.com/en-us/library/ms692342(v=VS.85).aspx">FaxJob</a> object. 
				<ol>
<li>Call the <a href="https://msdn.microsoft.com/en-us/library/ms686615(v=VS.85).aspx">CoCreateInstance</a> function to retrieve a pointer to an <a href="https://msdn.microsoft.com/en-us/library/ms692375(v=VS.85).aspx">IFaxServer</a> interface.</li>
<li>Call the <a href="https://msdn.microsoft.com/en-us/library/ms692315(v=VS.85).aspx">IFaxServer::Connect</a> method to connect to an active fax server. </li>
<li>Call the <a href="https://msdn.microsoft.com/en-us/library/ms692836(v=VS.85).aspx">IFaxServer::GetJobs</a> method to create and initialize a <a href="https://msdn.microsoft.com/en-us/library/ms692796(v=VS.85).aspx">FaxJobs</a> object for the connected fax server.</li>
<li>Call the <a href="https://msdn.microsoft.com/en-us/library/ms691382(v=VS.85).aspx">IFaxJobs::get_Count</a> method and then the <a href="https://msdn.microsoft.com/en-us/library/ms691271(v=VS.85).aspx">IFaxJobs::get_Item</a> method to retrieve <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface pointers for each child <a href="https://msdn.microsoft.com/en-us/library/ms692342(v=VS.85).aspx">FaxJob</a> object. (You can also call the <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">IUnknown::QueryInterface</a> method to retrieve an <b>IFaxJob</b> interface pointer.)</li>
<li>Use the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface pointer to call <b>IFaxJob</b> interface methods.</li>
<li>Call the <a href="https://msdn.microsoft.com/en-us/library/ms691936(v=VS.85).aspx">IFaxServer::Disconnect</a> method to disconnect from the fax server.</li>
<li>Call the <a href="https://msdn.microsoft.com/en-us/library/ms682317(v=VS.85).aspx">IUnknown::Release</a> method for each <a href="https://msdn.microsoft.com/en-us/library/ms692342(v=VS.85).aspx">FaxJob</a> object to allow the object to deallocate itself, and again to destroy the <a href="https://msdn.microsoft.com/en-us/library/ms692372(v=VS.85).aspx">IFaxJobs</a> interface pointer.</li>
</ol>





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>
 

 

