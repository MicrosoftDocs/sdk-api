---
UID: NN:faxcomex.IFaxServerNotify
title: IFaxServerNotify
author: windows-driver-content
description: The IFaxServerNotify interface is used for fax notifications.
old-location: fax\_mfax_ifaxservernotify.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_8dtl.htm
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: IFaxServerNotify, IFaxServerNotify interface [Fax Service], IFaxServerNotify interface [Fax Service], described, _mfax_ifaxservernotify, fax._mfax_ifaxservernotify, faxcomex/IFaxServerNotify
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
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Fxscomex.dll
api_name:
-	IFaxServerNotify
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxServerNotify interface


## -description


The <b>IFaxServerNotify</b> interface is used for fax notifications. The fax service calls <b>IFaxServerNotify</b> to send fax event notifications. Events include changes to fax server configuration and activity, changes to incoming and outgoing job queues, and changes to incoming and outgoing archives. For more information, see <a href="https://msdn.microsoft.com/a02d2bc4-bbee-4eb5-8e19-6032957155ce">Registering for Event Notifications</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxServerNotify</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFaxServerNotify</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFaxServerNotify</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c661dbfe-216b-4acd-b2cd-da8b8038128e">OnActivityLoggingConfigChange</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/c661dbfe-216b-4acd-b2cd-da8b8038128e">IFaxServerNotify::OnActivityLoggingConfigChange</a> method when there is a configuration change related to activity logging.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1b7e3dba-1dce-4364-a90f-aba6a46af53c">OnDevicesConfigChange</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/1b7e3dba-1dce-4364-a90f-aba6a46af53c">IFaxServerNotify::OnDevicesConfigChange</a> method when there is a change to a fax device configuration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9563affa-833d-41b3-bf3f-e43ed78949b5">OnDeviceStatusChange</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/9563affa-833d-41b3-bf3f-e43ed78949b5">IFaxServerNotify::OnDeviceStatusChange</a> method when there is a change to a fax device status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b73f349f-97c1-48f8-92ea-3ae958604f90">OnEventLoggingConfigChange</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/b73f349f-97c1-48f8-92ea-3ae958604f90">IFaxServerNotify::OnEventLoggingConfigChange</a> method when there is a configuration change related to event logging.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1d4f4c17-861c-4827-9331-bf40695d0796">OnIncomingArchiveConfigChange</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/1d4f4c17-861c-4827-9331-bf40695d0796">IFaxServerNotify::OnIncomingArchiveConfigChange</a> method when there is a configuration change related to the incoming fax archive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f296598-57a5-4329-afb6-f124ab7a47ec">OnIncomingJobAdded</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/2f296598-57a5-4329-afb6-f124ab7a47ec">IFaxServerNotify::OnIncomingJobAdded</a> method when an incoming fax job is added to the job queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/109f1f7d-f2e3-4db8-8800-3efa41b08942">OnIncomingJobChanged</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/109f1f7d-f2e3-4db8-8800-3efa41b08942">IFaxServerNotify::OnIncomingJobChanged</a> method when the status of an incoming fax job changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cbfd903c-15a9-46aa-9eb9-ce647c5d9b5a">OnIncomingJobRemoved</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/cbfd903c-15a9-46aa-9eb9-ce647c5d9b5a">IFaxServerNotify::OnIncomingJobRemoved</a> method when an incoming fax job is removed from the job queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d1997eaf-8e4c-4cd3-bdce-c8163170fd2c">OnIncomingMessageAdded</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/d1997eaf-8e4c-4cd3-bdce-c8163170fd2c">IFaxServerNotify::OnIncomingMessageAdded</a> method when an incoming message is added to the inbound fax archive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9e5f0f87-3802-4e0c-aa6f-cb8614dbc791">OnIncomingMessageRemoved</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/9e5f0f87-3802-4e0c-aa6f-cb8614dbc791">IFaxServerNotify::OnIncomingMessageRemoved</a> method when an incoming message is removed from the inbound fax archive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/07bdc543-d80c-4929-84d2-c60126c0407f">OnNewCall</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/07bdc543-d80c-4929-84d2-c60126c0407f">IFaxServerNotify::OnNewCall</a> method when there is a new incoming fax call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8bfb5dbb-930f-4870-a2cf-630ffdd79fe0">OnOutboundRoutingGroupsConfigChange</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/8bfb5dbb-930f-4870-a2cf-630ffdd79fe0">IFaxServerNotify::OnOutboundRoutingGroupsConfigChange</a> method when there is a configuration change related to outbound fax routing groups.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/03c1368d-1bce-427c-aae1-eca584d5e741">OnOutboundRoutingRulesConfigChange</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/03c1368d-1bce-427c-aae1-eca584d5e741">IFaxServerNotify::OnOutboundRoutingRulesConfigChange</a> method when there is a configuration change related to outbound fax routing rules.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c4f5ba4a-7d68-4103-9297-4b3479e08c1e">OnOutgoingArchiveConfigChange</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/c4f5ba4a-7d68-4103-9297-4b3479e08c1e">IFaxServerNotify::OnOutgoingArchiveConfigChange</a> method when there is a configuration change related to the outgoing fax archive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/af0ded73-6954-4f66-b1b7-6b1dd6a98495">OnOutgoingJobAdded</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/af0ded73-6954-4f66-b1b7-6b1dd6a98495">IFaxServerNotify::OnOutgoingJobAdded</a> method when an outgoing fax job is added to the job queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/132747ed-04b4-4803-976c-5274d8c9f73d">OnOutgoingJobChanged</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/132747ed-04b4-4803-976c-5274d8c9f73d">IFaxServerNotify::OnOutgoingJobChanged</a> method when the status of an outgoing fax job changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7211cd34-7a32-47d2-b7ce-e40ae1183941">OnOutgoingJobRemoved</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/7211cd34-7a32-47d2-b7ce-e40ae1183941">IFaxServerNotify::OnOutgoingJobRemoved</a> method when an outgoing fax job is removed from the job queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/410f01cd-7bd2-4e52-a76b-a4be262c0dd6">OnOutgoingMessageAdded</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/410f01cd-7bd2-4e52-a76b-a4be262c0dd6">IFaxServerNotify::OnOutgoingMessageAdded</a> method when an outgoing message is added to the outbound fax archive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/31cf469c-fe78-4763-968e-4a229d149c96">OnOutgoingMessageRemoved</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/31cf469c-fe78-4763-968e-4a229d149c96">IFaxServerNotify::OnOutgoingMessageRemoved</a> method when an outgoing message is removed from the fax outbound archive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/50132344-d111-4064-9d71-6c5460c81860">OnOutgoingQueueConfigChange</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/50132344-d111-4064-9d71-6c5460c81860">IFaxServerNotify::OnOutgoingQueueConfigChange</a> method when there is a configuration change related to the outgoing fax job queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a5dea99b-9b77-48ab-99d2-1ed4f55b905d">OnQueuesStatusChange</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/a5dea99b-9b77-48ab-99d2-1ed4f55b905d">IFaxServerNotify::OnQueuesStatusChange</a> method when there is a change in the fax job queue status.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ce70584-0049-46eb-aba1-2e03fad1d83a">OnReceiptOptionsChange</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/4ce70584-0049-46eb-aba1-2e03fad1d83a">IFaxServerNotify::OnReceiptOptionsChange</a> method when there is a change that relates to receipt configuration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/43df68f5-ae83-4391-bab0-f68aea3e8bae">OnSecurityConfigChange</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/43df68f5-ae83-4391-bab0-f68aea3e8bae">IFaxServerNotify::OnSecurityConfigChange</a> method when there is a configuration change related to security.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b5946cf0-2a01-4245-8ba3-f981db98fa7e">OnServerActivityChange</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/b5946cf0-2a01-4245-8ba3-f981db98fa7e">IFaxServerNotify::OnServerActivityChange</a> method when the fax service activity and status changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e6404bef-3f2a-4a44-a6a0-701975f122c4">OnServerShutDown</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/e6404bef-3f2a-4a44-a6a0-701975f122c4">IFaxServerNotify::OnServerShutDown</a> method when the fax service shuts down.

</td>
</tr>
</table> 


## -remarks



<h3><a id="To_Use_Fax_Notification_Events_with_Visual_Basic"></a><a id="to_use_fax_notification_events_with_visual_basic"></a><a id="TO_USE_FAX_NOTIFICATION_EVENTS_WITH_VISUAL_BASIC"></a>To Use Fax Notification Events with Visual Basic</h3>
Use the following syntax when creating the root FaxServer object:


<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
Dim WithEvents objFaxServer As FaxServer
</pre>
</td>
</tr>
</table></span></div>


For an example, see <a href="https://msdn.microsoft.com/3a9f42fa-383a-4072-92a6-b59f7940ab04">Registering for Fax Events</a>.
            

<h3><a id="To_Use_Fax_Notification_Events_with_C__"></a><a id="to_use_fax_notification_events_with_c__"></a><a id="TO_USE_FAX_NOTIFICATION_EVENTS_WITH_C__"></a>To Use Fax Notification Events with C++</h3>

			A fax client application must implement <b>IFaxServerNotify</b> and pass the fax service the pointer to an <b>IFaxServerNotify</b> interface.
            



