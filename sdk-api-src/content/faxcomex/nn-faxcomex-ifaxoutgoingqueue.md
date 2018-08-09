---
UID: NN:faxcomex.IFaxOutgoingQueue
title: IFaxOutgoingQueue
author: windows-sdk-content
description: The IFaxOutgoingQueue interface defines a FaxOutgoingQueue configuration object used by a fax client application to set and retrieve the configuration parameters on the outbound fax queue on a fax server.
old-location: fax\_mfax_faxoutgoingqueue_cpp.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_0dyd_cpp.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: IFaxOutgoingQueue, IFaxOutgoingQueue interface [Fax Service], IFaxOutgoingQueue interface [Fax Service],described, _mfax_faxoutgoingqueue_cpp, fax._mfax_faxoutgoingqueue_cpp, faxcomex/IFaxOutgoingQueue
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
 - IFaxOutgoingQueue
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxOutgoingQueue interface


## -description


The <b>IFaxOutgoingQueue</b> interface defines a <a href="https://msdn.microsoft.com/bad77c9e-2ae5-41a6-ace3-b4b92eb66cc2">FaxOutgoingQueue</a> configuration object used by a fax client application to set and retrieve the configuration parameters on the outbound fax queue on a fax server. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxOutgoingQueue</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFaxOutgoingQueue</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFaxOutgoingQueue</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2ec26d46-91b4-44a1-840a-5ef9c556c303">GetJob</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/2ec26d46-91b4-44a1-840a-5ef9c556c303">IFaxOutgoingQueue::GetJob</a> method returns an outbound fax job in the job queue according to its ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb17e3ba-dcae-45d9-8c7f-eb12c611b69c">GetJobs</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/fb17e3ba-dcae-45d9-8c7f-eb12c611b69c">IFaxOutgoingQueue::GetJobs</a> method returns a collection of the outbound fax jobs in the job queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/903cd111-d3bb-4871-b308-ae5ba8cfbf73">Refresh</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/903cd111-d3bb-4871-b308-ae5ba8cfbf73">IFaxOutgoingQueue::Refresh</a> method refreshes <a href="https://msdn.microsoft.com/bad77c9e-2ae5-41a6-ace3-b4b92eb66cc2">FaxOutgoingQueue</a> object information from the fax server. When the <b>IFaxOutgoingQueue::Refresh</b> method is called, any configuration changes made after the last <a href="https://msdn.microsoft.com/cbb71582-cff9-4bba-aea8-9c88be61ea47">IFaxOutgoingQueue::Save</a> method call are lost.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926944">Save</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/cbb71582-cff9-4bba-aea8-9c88be61ea47">IFaxOutgoingQueue::Save</a> method saves the <a href="https://msdn.microsoft.com/bad77c9e-2ae5-41a6-ace3-b4b92eb66cc2">FaxOutgoingQueue</a> object data.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxOutgoingQueue</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e88d86b2-faac-4908-93ef-835212bc7613">AgeLimit</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/e88d86b2-faac-4908-93ef-835212bc7613">IFaxOutgoingQueue::get_AgeLimit</a> property is a value that indicates the number of days that the fax service retains an unsent job in the fax job queue. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/f8d04607-f76b-4c72-a2f9-c7e31b17beca">AllowPersonalCoverPages</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The AllowPersonalCoverPages property is a Boolean value that indicates whether fax client applications can include a user-designed cover page with fax transmissions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8744ca4b-feda-419e-9211-afdb85a5023d">Blocked</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/8744ca4b-feda-419e-9211-afdb85a5023d">IFaxOutgoingQueue::get_Blocked</a> property is a Boolean value that indicates whether the job queue for outgoing faxes is blocked. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/b7af7371-b1c3-4b41-b8e8-b0b6a1149b8d">Branding</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/b7af7371-b1c3-4b41-b8e8-b0b6a1149b8d">IFaxOutgoingQueue::get_Branding</a> property is a Boolean value that indicates whether the fax service generates a brand (banner) at the top of outgoing fax transmissions. A brand contains transmission-related information, such as the transmitting station identifier, date, time, and page count.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5bb282da-3226-4c9d-ab75-82a587b0a56f">DiscountRateEnd</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/5bb282da-3226-4c9d-ab75-82a587b0a56f">IFaxOutgoingQueue::get_DiscountRateEnd</a> property is a value that indicates the time at which the discount period for transmitting faxes ends. The discount period applies to outgoing faxes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8df89f09-8fba-4bad-a516-82ab471d189e">DiscountRateStart</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/8df89f09-8fba-4bad-a516-82ab471d189e">IFaxOutgoingQueue::get_DiscountRateStart</a> property is a value that indicates the time at which the discount period for transmitting faxes begins. The discount period applies to outgoing faxes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/f525146d-2e6a-4410-9e89-f4ce3e37e105">Paused</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/f525146d-2e6a-4410-9e89-f4ce3e37e105">IFaxOutgoingQueue::get_Paused</a> property is a Boolean value that indicates whether the job queue for outgoing faxes is paused. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/94432d7a-42ed-4d8d-92c0-930e02188aa4">Retries</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/94432d7a-42ed-4d8d-92c0-930e02188aa4">IFaxOutgoingQueue::get_Retries</a> property is a value that indicates the number of times that the fax service attempts to retransmit an outgoing fax when the initial transmission fails.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/ab3c303d-7c89-46d2-8304-75146ebfaf4c">RetryDelay</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/ab3c303d-7c89-46d2-8304-75146ebfaf4c">IFaxOutgoingQueue::get_RetryDelay</a> property is a value that indicates the time interval, in minutes, that the fax service waits before attempting to retransmit an outbound fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/0ea89e91-9c9f-47b8-9196-596536e8f8c2">UseDeviceTSID</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/0ea89e91-9c9f-47b8-9196-596536e8f8c2">IFaxOutgoingQueue::get_UseDeviceTSID</a> property is a Boolean value that indicates whether the fax service uses the device TSID instead of a sender TSID. 

</td>
</tr>
</table> 


## -remarks



A default implementation of <b>IFaxOutgoingQueue</b> is provided as the <a href="https://msdn.microsoft.com/bad77c9e-2ae5-41a6-ace3-b4b92eb66cc2">FaxOutgoingQueue</a> object. 



