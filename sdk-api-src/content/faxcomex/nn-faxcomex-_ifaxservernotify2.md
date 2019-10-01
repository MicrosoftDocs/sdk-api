---
UID: NN:faxcomex._IFaxServerNotify2
title: _IFaxServerNotify2 (faxcomex.h)
author: windows-sdk-content
description: The IFaxServerNotify2 interface is used for fax notifications.
old-location: fax\_mfax_ifaxservernotify2.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxservernotify2\faxinto_z_ifaxservernotify2.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFaxServerNotify2, IFaxServerNotify2 interface [Fax Service], IFaxServerNotify2 interface [Fax Service],described, IIFaxServerNotify2, _mfax_ifaxservernotify2, fax._mfax_ifaxservernotify2, faxcomex/IFaxServerNotify2
ms.topic: interface
f1_keywords: 
 - "faxcomex/IFaxServerNotify2"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# _IFaxServerNotify2 interface


## -description


The <b>IFaxServerNotify2</b> interface is used for fax notifications. The fax service calls <b>IFaxServerNotify2</b> to send fax event notifications. Events include changes to fax server configuration and activity, changes to incoming and outgoing job queues, and changes to incoming and outgoing archives. For more information, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-registering-for-event-notifications">Registering for Event Notifications</a>.

The <b>IFaxServerNotify2</b> interface supports all the same methods as the <a href="https://docs.microsoft.com/en-us/windows/desktop/api/faxcomex/nn-faxcomex-ifaxservernotify2">IFaxServerNotify</a> interface and the additional method <a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-ongeneralserverconfigchanged">OnGeneralServerConfigChanged</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxServerNotify2</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxServerNotify2</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-onactivityloggingconfigchange">OnActivityLoggingConfigChange</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-onactivityloggingconfigchange">IFaxServerNotify2::OnActivityLoggingConfigChange</a> method when there is a configuration change related to activity logging.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-ondevicesconfigchange">OnDevicesConfigChange</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-ondevicesconfigchange">IFaxServerNotify2::OnDevicesConfigChange</a> method when there is a change to a fax device configuration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-ondevicestatuschange">OnDeviceStatusChange</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-ondevicestatuschange">IFaxServerNotify2::OnDeviceStatusChange</a> method when there is a change to a fax device status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-oneventloggingconfigchange">OnEventLoggingConfigChange</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-oneventloggingconfigchange">IFaxServerNotify2::OnEventLoggingConfigChange</a> method when there is a configuration change related to event logging.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-ongeneralserverconfigchanged">OnGeneralServerConfigChanged</a>
</td>
<td align="left" width="63%">
Called by the fax service when the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxserver2-configuration-vb">IFaxServer2::Configuration</a> property changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-onincomingarchiveconfigchange">OnIncomingArchiveConfigChange</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-onincomingarchiveconfigchange">IFaxServerNotify2::OnIncomingArchiveConfigChange</a> method when there is a configuration change related to the incoming fax archive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-onincomingjobadded">OnIncomingJobAdded</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-onincomingjobadded">IFaxServerNotify2::OnIncomingJobAdded</a> method when an incoming fax job is added to the job queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-onincomingjobchanged">OnIncomingJobChanged</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-onincomingjobchanged">IFaxServerNotify2::OnIncomingJobChanged</a> method when the status of an incoming fax job changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-onincomingjobremoved">OnIncomingJobRemoved</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-onincomingjobremoved">IFaxServerNotify2::OnIncomingJobRemoved</a> method when an incoming fax job is removed from the job queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-onincomingmessageadded">OnIncomingMessageAdded</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-onincomingmessageadded">IFaxServerNotify2::OnIncomingMessageAdded</a> method when an incoming message is added to the inbound fax archive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-onincomingmessageremoved">OnIncomingMessageRemoved</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-onincomingmessageremoved">IFaxServerNotify2::OnIncomingMessageRemoved</a> method when an incoming message is removed from the inbound fax archive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-onnewcall">OnNewCall</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-onnewcall">IFaxServerNotify2::OnNewCall</a> method when there is a new incoming fax call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-onoutboundroutinggroupsconfigchange">OnOutboundRoutingGroupsConfigChange</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-onoutboundroutinggroupsconfigchange">IFaxServerNotify2::OnOutboundRoutingGroupsConfigChange</a> method when there is a configuration change related to outbound fax routing groups.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-onoutboundroutingrulesconfigchange">OnOutboundRoutingRulesConfigChange</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-onoutboundroutingrulesconfigchange">IFaxServerNotify2::OnOutboundRoutingRulesConfigChange</a> method when there is a configuration change related to outbound fax routing rules.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-onoutgoingarchiveconfigchange">OnOutgoingArchiveConfigChange</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-onoutgoingarchiveconfigchange">IFaxServerNotify2::OnOutgoingArchiveConfigChange</a> method when there is a configuration change related to the outgoing fax archive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-onoutgoingjobadded">OnOutgoingJobAdded</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-onoutgoingjobadded">IFaxServerNotify2::OnOutgoingJobAdded</a> method when an outgoing fax job is added to the job queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-onoutgoingjobchanged">OnOutgoingJobChanged</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-onoutgoingjobchanged">IFaxServerNotify2::OnOutgoingJobChanged</a> method when the status of an outgoing fax job changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-onoutgoingjobremoved">OnOutgoingJobRemoved</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-onoutgoingjobremoved">IFaxServerNotify2::OnOutgoingJobRemoved</a> method when an outgoing fax job is removed from the job queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-onoutgoingmessageadded">OnOutgoingMessageAdded</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-onoutgoingmessageadded">IFaxServerNotify2::OnOutgoingMessageAdded</a> method when an outgoing message is added to the outbound fax archive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-onoutgoingmessageremoved">OnOutgoingMessageRemoved</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-onoutgoingmessageremoved">IFaxServerNotify2::OnOutgoingMessageRemoved</a> method when an outgoing message is removed from the fax outbound archive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-onoutgoingqueueconfigchange">OnOutgoingQueueConfigChange</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-onoutgoingqueueconfigchange">IFaxServerNotify2::OnOutgoingQueueConfigChange</a> method when there is a configuration change related to the outgoing fax job queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-onqueuesstatuschange">OnQueuesStatusChange</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-onqueuesstatuschange">IFaxServerNotify2::OnQueuesStatusChange</a> method when there is a change in the fax job queue status.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-onreceiptoptionschange">OnReceiptOptionsChange</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-onreceiptoptionschange">IFaxServerNotify2::OnReceiptOptionsChange</a> method when there is a change that relates to receipt configuration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-onsecurityconfigchange">OnSecurityConfigChange</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-onsecurityconfigchange">IFaxServerNotify2::OnSecurityConfigChange</a> method when there is a configuration change related to security.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-onserveractivitychange">OnServerActivityChange</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-onserveractivitychange">IFaxServerNotify2::OnServerActivityChange</a> method when the fax service activity and status changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-onservershutdown">OnServerShutDown</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nf-faxcomex-_ifaxservernotify2-onservershutdown">IFaxServerNotify2::OnServerShutDown</a> method when the fax service shuts down.

</td>
</tr>
</table> 


## -remarks



<h3><a id="To_Use_Fax_Notification_Events_with_Visual_Basic"></a><a id="to_use_fax_notification_events_with_visual_basic"></a><a id="TO_USE_FAX_NOTIFICATION_EVENTS_WITH_VISUAL_BASIC"></a>To Use Fax Notification Events with Visual Basic</h3>
Use the following syntax when creating the root FaxServer2 object:



```

Dim WithEvents objFaxServer2 As FaxServer2

```




For an example, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-registering-for-fax-events">Registering for Fax Events</a>.
            

<h3><a id="To_Use_Fax_Notification_Events_with_C__"></a><a id="to_use_fax_notification_events_with_c__"></a><a id="TO_USE_FAX_NOTIFICATION_EVENTS_WITH_C__"></a>To Use Fax Notification Events with C++</h3>
A fax client application must implement <b>IFaxServerNotify2</b> and pass the fax service the pointer to an <b>IFaxServerNotify2</b> interface.
            



