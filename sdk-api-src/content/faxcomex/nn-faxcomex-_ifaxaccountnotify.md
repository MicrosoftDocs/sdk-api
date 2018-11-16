---
UID: NN:faxcomex._IFaxAccountNotify
title: "_IFaxAccountNotify"
author: windows-sdk-content
description: Called by the fax service to send event notifications about particular fax accounts. This property sends event notifications. Events include changes to incoming and outgoing job queues, and changes to incoming and outgoing archives.
old-location: fax\_mfax_ifaxaccountnotify.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccountnotify\faxinto_z_ifaxaccountnotify.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IFaxAccountNotify, IFaxAccountNotify interface [Fax Service], IFaxAccountNotify interface [Fax Service],described, IIFaxAccountNotify, _IFaxAccountNotify, _mfax_ifaxaccountnotify, fax._mfax_ifaxaccountnotify, faxcomex/_IFaxAccountNotify
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IFaxAccountNotify
 - IIFaxAccountNotify
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# _IFaxAccountNotify interface


## -description


Called by the fax service to send event notifications about particular fax accounts. This property sends event notifications. Events include changes to incoming and outgoing job queues, and changes to incoming and outgoing archives.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxAccountNotify</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>_IFaxAccountNotify</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFaxAccountNotify</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9b4d1e44-f28f-4472-b39d-e8a8c05e4af3">OnIncomingJobAdded</a>
</td>
<td align="left" width="63%">
Called by the fax service when an incoming fax job is added to the job queue for a particular fax account.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bfbf9415-4a08-4d97-998c-71c184221ab7">OnIncomingJobChanged</a>
</td>
<td align="left" width="63%">
Called by the fax service when the status of an incoming fax job for a particular fax account changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bf3c6171-d7a9-4db5-872e-dbc08353602e">OnIncomingJobRemoved</a>
</td>
<td align="left" width="63%">
Called by the fax service when an incoming fax job is removed from the job queue of a particular fax account.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e320f56c-ccc9-481f-a4df-d106d1c975cf">OnIncomingMessageAdded</a>
</td>
<td align="left" width="63%">
Called by the fax service when an incoming message is added to the inbound fax archive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fc3b88cc-e157-4fe5-aed0-e170b59b9e7a">OnIncomingMessageRemoved</a>
</td>
<td align="left" width="63%">
Called by the fax service when an incoming message is removed from the inbound fax archive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6219b321-8fbb-46f6-8626-c5fae2e2afb0">OnOngoingMessageRemoved</a>
</td>
<td align="left" width="63%">
Called by the fax service when an outgoing message is removed from the outbound fax archive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2c9aa8a9-1d3c-4cfe-8cfd-69cc06036550">OnOutgoingJobAdded</a>
</td>
<td align="left" width="63%">
Called by the fax service when an outgoing fax job is added to the job queue for a particular fax account.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/84d5114a-135d-4f37-b979-4b3ab196bd5e">OnOutgoingJobChanged</a>
</td>
<td align="left" width="63%">
Called by the fax service when the status of an outgoing fax job for a particular fax account changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3fefb1a7-9cd7-4170-8a05-3285941c640d">OnOutgoingJobRemoved</a>
</td>
<td align="left" width="63%">
Called by the fax service when an outgoing fax job is removed from the job queue of a particular fax account.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e0b71e45-c252-4390-bac8-36ec39296142">OnOutgoingMessageAdded</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/e0b71e45-c252-4390-bac8-36ec39296142">IFaxAccountNotify::OnOutgoingMessageAdded</a> method when an outgoing message is added to the outbound fax archive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/292e5635-9a21-46b9-9c13-27a474181da6">OnServerShutDown</a>
</td>
<td align="left" width="63%">
Called by the fax service when it shuts down. 

</td>
</tr>
</table> 


## -remarks



<h3><a id="To_Use_Fax_Notification_Events_with_Visual_Basic"></a><a id="to_use_fax_notification_events_with_visual_basic"></a><a id="TO_USE_FAX_NOTIFICATION_EVENTS_WITH_VISUAL_BASIC"></a>To Use Fax Notification Events with Visual Basic</h3>
Use the following syntax when creating the <a href="https://msdn.microsoft.com/438a35bd-d08b-4b29-95e5-81ff5c23e92b">IFaxAccount</a> object:


<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
Dim WithEvents objFaxAccount As FaxAccount
</pre>
</td>
</tr>
</table></span></div>
<h3><a id="To_Use_Fax_Notification_Events_with_C__"></a><a id="to_use_fax_notification_events_with_c__"></a><a id="TO_USE_FAX_NOTIFICATION_EVENTS_WITH_C__"></a>To Use Fax Notification Events with C++</h3>
A fax client application must implement <b>IFaxAccountNotify</b> and pass the fax service the pointer to an <b>IFaxAccountNotify</b> interface.
            



