---
UID: NN:faxcomex.IFaxOutgoingQueue
title: IFaxOutgoingQueue (faxcomex.h)
author: windows-sdk-content
description: The IFaxOutgoingQueue interface defines a FaxOutgoingQueue configuration object used by a fax client application to set and retrieve the configuration parameters on the outbound fax queue on a fax server.
old-location: fax\_mfax_faxoutgoingqueue_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_0dyd_cpp.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFaxOutgoingQueue, IFaxOutgoingQueue interface [Fax Service], IFaxOutgoingQueue interface [Fax Service],described, _mfax_faxoutgoingqueue_cpp, fax._mfax_faxoutgoingqueue_cpp, faxcomex/IFaxOutgoingQueue
ms.topic: interface
f1_keywords: 
 - "faxcomex/IFaxOutgoingQueue"
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
 - IFaxOutgoingQueue
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxOutgoingQueue interface


## -description


The <b>IFaxOutgoingQueue</b> interface defines a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingqueue">FaxOutgoingQueue</a> configuration object used by a fax client application to set and retrieve the configuration parameters on the outbound fax queue on a fax server. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxOutgoingQueue</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxOutgoingQueue</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxoutgoingqueue-getjob">GetJob</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxoutgoingqueue-getjob">IFaxOutgoingQueue::GetJob</a> method returns an outbound fax job in the job queue according to its ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingqueue-getjobs-vb">GetJobs</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingqueue-getjobs-vb">IFaxOutgoingQueue::GetJobs</a> method returns a collection of the outbound fax jobs in the job queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingqueue-refresh-vb">Refresh</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingqueue-refresh-vb">IFaxOutgoingQueue::Refresh</a> method refreshes <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingqueue">FaxOutgoingQueue</a> object information from the fax server. When the <b>IFaxOutgoingQueue::Refresh</b> method is called, any configuration changes made after the last <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingqueue-save-vb">IFaxOutgoingQueue::Save</a> method call are lost.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingqueue-save-vb">Save</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingqueue-save-vb">IFaxOutgoingQueue::Save</a> method saves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingqueue">FaxOutgoingQueue</a> object data.

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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingqueue-agelimit-vb">AgeLimit</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingqueue-agelimit-vb">IFaxOutgoingQueue::get_AgeLimit</a> property is a value that indicates the number of days that the fax service retains an unsent job in the fax job queue. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingqueue-allowpersonalcoverpages-vb">AllowPersonalCoverPages</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingqueue-blocked-vb">Blocked</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingqueue-blocked-vb">IFaxOutgoingQueue::get_Blocked</a> property is a Boolean value that indicates whether the job queue for outgoing faxes is blocked. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingqueue-branding-vb">Branding</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingqueue-branding-vb">IFaxOutgoingQueue::get_Branding</a> property is a Boolean value that indicates whether the fax service generates a brand (banner) at the top of outgoing fax transmissions. A brand contains transmission-related information, such as the transmitting station identifier, date, time, and page count.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingqueue-discountrateend-vb">DiscountRateEnd</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingqueue-discountrateend-vb">IFaxOutgoingQueue::get_DiscountRateEnd</a> property is a value that indicates the time at which the discount period for transmitting faxes ends. The discount period applies to outgoing faxes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingqueue-discountratestart-vb">DiscountRateStart</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingqueue-discountratestart-vb">IFaxOutgoingQueue::get_DiscountRateStart</a> property is a value that indicates the time at which the discount period for transmitting faxes begins. The discount period applies to outgoing faxes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingqueue-paused-vb">Paused</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingqueue-paused-vb">IFaxOutgoingQueue::get_Paused</a> property is a Boolean value that indicates whether the job queue for outgoing faxes is paused. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingqueue-retries-vb">Retries</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingqueue-retries-vb">IFaxOutgoingQueue::get_Retries</a> property is a value that indicates the number of times that the fax service attempts to retransmit an outgoing fax when the initial transmission fails.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingqueue-retrydelay-vb">RetryDelay</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingqueue-retrydelay-vb">IFaxOutgoingQueue::get_RetryDelay</a> property is a value that indicates the time interval, in minutes, that the fax service waits before attempting to retransmit an outbound fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingqueue-usedevicetsid-vb">UseDeviceTSID</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingqueue-usedevicetsid-vb">IFaxOutgoingQueue::get_UseDeviceTSID</a> property is a Boolean value that indicates whether the fax service uses the device TSID instead of a sender TSID. 

</td>
</tr>
</table> 


## -remarks



A default implementation of <b>IFaxOutgoingQueue</b> is provided as the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingqueue">FaxOutgoingQueue</a> object. 



