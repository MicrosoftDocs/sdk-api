---
UID: NN:faxcomex._IFaxServerNotify2
title: "_IFaxServerNotify2"
author: windows-sdk-content
description: The IFaxServerNotify2 interface is used for fax notifications.
old-location: fax\_mfax_ifaxservernotify2.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxservernotify2\faxinto_z_ifaxservernotify2.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IFaxServerNotify2, IFaxServerNotify2 interface [Fax Service], IFaxServerNotify2 interface [Fax Service],described, IIFaxServerNotify2, _mfax_ifaxservernotify2, fax._mfax_ifaxservernotify2, faxcomex/IFaxServerNotify2
ms.prod: windows
ms.technology: windows-sdk
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
 - IFaxServerNotify2
 - IIFaxServerNotify2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# _IFaxServerNotify2 interface


## -description


The <b>IFaxServerNotify2</b> interface is used for fax notifications. The fax service calls <b>IFaxServerNotify2</b> to send fax event notifications. Events include changes to fax server configuration and activity, changes to incoming and outgoing job queues, and changes to incoming and outgoing archives. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms693008(v=VS.85).aspx">Registering for Event Notifications</a>.

The <b>IFaxServerNotify2</b> interface supports all the same methods as the <a href="https://msdn.microsoft.com/en-us/library/ms690086(v=VS.85).aspx">IFaxServerNotify</a> interface and the additional method <a href="https://msdn.microsoft.com/en-us/library/Aa358972(v=VS.85).aspx">OnGeneralServerConfigChanged</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxServerNotify2</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IFaxServerNotify2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFaxServerNotify2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa358835(v=VS.85).aspx">OnActivityLoggingConfigChange</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/en-us/library/Aa358835(v=VS.85).aspx">IFaxServerNotify2::OnActivityLoggingConfigChange</a> method when there is a configuration change related to activity logging.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa358836(v=VS.85).aspx">OnDevicesConfigChange</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/en-us/library/Aa358836(v=VS.85).aspx">IFaxServerNotify2::OnDevicesConfigChange</a> method when there is a change to a fax device configuration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa358837(v=VS.85).aspx">OnDeviceStatusChange</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/en-us/library/Aa358837(v=VS.85).aspx">IFaxServerNotify2::OnDeviceStatusChange</a> method when there is a change to a fax device status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa358838(v=VS.85).aspx">OnEventLoggingConfigChange</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/en-us/library/Aa358838(v=VS.85).aspx">IFaxServerNotify2::OnEventLoggingConfigChange</a> method when there is a configuration change related to event logging.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa358972(v=VS.85).aspx">OnGeneralServerConfigChanged</a>
</td>
<td align="left" width="63%">
Called by the fax service when the <a href="https://msdn.microsoft.com/en-us/library/Aa358973(v=VS.85).aspx">IFaxServer2::Configuration</a> property changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa358839(v=VS.85).aspx">OnIncomingArchiveConfigChange</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/en-us/library/Aa358839(v=VS.85).aspx">IFaxServerNotify2::OnIncomingArchiveConfigChange</a> method when there is a configuration change related to the incoming fax archive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa358840(v=VS.85).aspx">OnIncomingJobAdded</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/en-us/library/Aa358840(v=VS.85).aspx">IFaxServerNotify2::OnIncomingJobAdded</a> method when an incoming fax job is added to the job queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa358841(v=VS.85).aspx">OnIncomingJobChanged</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/en-us/library/Aa358841(v=VS.85).aspx">IFaxServerNotify2::OnIncomingJobChanged</a> method when the status of an incoming fax job changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa358842(v=VS.85).aspx">OnIncomingJobRemoved</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/en-us/library/Aa358842(v=VS.85).aspx">IFaxServerNotify2::OnIncomingJobRemoved</a> method when an incoming fax job is removed from the job queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa358843(v=VS.85).aspx">OnIncomingMessageAdded</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/en-us/library/Aa358843(v=VS.85).aspx">IFaxServerNotify2::OnIncomingMessageAdded</a> method when an incoming message is added to the inbound fax archive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa358844(v=VS.85).aspx">OnIncomingMessageRemoved</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/en-us/library/Aa358844(v=VS.85).aspx">IFaxServerNotify2::OnIncomingMessageRemoved</a> method when an incoming message is removed from the inbound fax archive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa358845(v=VS.85).aspx">OnNewCall</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/en-us/library/Aa358845(v=VS.85).aspx">IFaxServerNotify2::OnNewCall</a> method when there is a new incoming fax call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa358846(v=VS.85).aspx">OnOutboundRoutingGroupsConfigChange</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/en-us/library/Aa358846(v=VS.85).aspx">IFaxServerNotify2::OnOutboundRoutingGroupsConfigChange</a> method when there is a configuration change related to outbound fax routing groups.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa358847(v=VS.85).aspx">OnOutboundRoutingRulesConfigChange</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/en-us/library/Aa358847(v=VS.85).aspx">IFaxServerNotify2::OnOutboundRoutingRulesConfigChange</a> method when there is a configuration change related to outbound fax routing rules.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa358848(v=VS.85).aspx">OnOutgoingArchiveConfigChange</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/en-us/library/Aa358848(v=VS.85).aspx">IFaxServerNotify2::OnOutgoingArchiveConfigChange</a> method when there is a configuration change related to the outgoing fax archive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa358849(v=VS.85).aspx">OnOutgoingJobAdded</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/en-us/library/Aa358849(v=VS.85).aspx">IFaxServerNotify2::OnOutgoingJobAdded</a> method when an outgoing fax job is added to the job queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa358850(v=VS.85).aspx">OnOutgoingJobChanged</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/en-us/library/Aa358850(v=VS.85).aspx">IFaxServerNotify2::OnOutgoingJobChanged</a> method when the status of an outgoing fax job changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa358851(v=VS.85).aspx">OnOutgoingJobRemoved</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/en-us/library/Aa358851(v=VS.85).aspx">IFaxServerNotify2::OnOutgoingJobRemoved</a> method when an outgoing fax job is removed from the job queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa358852(v=VS.85).aspx">OnOutgoingMessageAdded</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/en-us/library/Aa358852(v=VS.85).aspx">IFaxServerNotify2::OnOutgoingMessageAdded</a> method when an outgoing message is added to the outbound fax archive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa358853(v=VS.85).aspx">OnOutgoingMessageRemoved</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/en-us/library/Aa358853(v=VS.85).aspx">IFaxServerNotify2::OnOutgoingMessageRemoved</a> method when an outgoing message is removed from the fax outbound archive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa358854(v=VS.85).aspx">OnOutgoingQueueConfigChange</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/en-us/library/Aa358854(v=VS.85).aspx">IFaxServerNotify2::OnOutgoingQueueConfigChange</a> method when there is a configuration change related to the outgoing fax job queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa358855(v=VS.85).aspx">OnQueuesStatusChange</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/en-us/library/Aa358855(v=VS.85).aspx">IFaxServerNotify2::OnQueuesStatusChange</a> method when there is a change in the fax job queue status.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa358856(v=VS.85).aspx">OnReceiptOptionsChange</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/en-us/library/Aa358856(v=VS.85).aspx">IFaxServerNotify2::OnReceiptOptionsChange</a> method when there is a change that relates to receipt configuration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa358857(v=VS.85).aspx">OnSecurityConfigChange</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/en-us/library/Aa358857(v=VS.85).aspx">IFaxServerNotify2::OnSecurityConfigChange</a> method when there is a configuration change related to security.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa358858(v=VS.85).aspx">OnServerActivityChange</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/en-us/library/Aa358858(v=VS.85).aspx">IFaxServerNotify2::OnServerActivityChange</a> method when the fax service activity and status changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa358859(v=VS.85).aspx">OnServerShutDown</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/en-us/library/Aa358859(v=VS.85).aspx">IFaxServerNotify2::OnServerShutDown</a> method when the fax service shuts down.

</td>
</tr>
</table> 


## -remarks



<h3><a id="To_Use_Fax_Notification_Events_with_Visual_Basic"></a><a id="to_use_fax_notification_events_with_visual_basic"></a><a id="TO_USE_FAX_NOTIFICATION_EVENTS_WITH_VISUAL_BASIC"></a>To Use Fax Notification Events with Visual Basic</h3>
Use the following syntax when creating the root FaxServer2 object:



```

Dim WithEvents objFaxServer2 As FaxServer2

```




For an example, see <a href="https://msdn.microsoft.com/en-us/library/ms693013(v=VS.85).aspx">Registering for Fax Events</a>.
            

<h3><a id="To_Use_Fax_Notification_Events_with_C__"></a><a id="to_use_fax_notification_events_with_c__"></a><a id="TO_USE_FAX_NOTIFICATION_EVENTS_WITH_C__"></a>To Use Fax Notification Events with C++</h3>
A fax client application must implement <b>IFaxServerNotify2</b> and pass the fax service the pointer to an <b>IFaxServerNotify2</b> interface.
            



