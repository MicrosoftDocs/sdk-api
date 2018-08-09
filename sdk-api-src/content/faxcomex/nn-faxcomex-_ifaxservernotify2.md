---
UID: NN:faxcomex._IFaxServerNotify2
title: "_IFaxServerNotify2"
author: windows-sdk-content
description: The IFaxServerNotify2 interface is used for fax notifications.
old-location: fax\_mfax_ifaxservernotify2.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxservernotify2\faxinto_z_ifaxservernotify2.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
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
 - IFaxServerNotify2
 - IIFaxServerNotify2
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# _IFaxServerNotify2 interface


## -description


The <b>IFaxServerNotify2</b> interface is used for fax notifications. The fax service calls <b>IFaxServerNotify2</b> to send fax event notifications. Events include changes to fax server configuration and activity, changes to incoming and outgoing job queues, and changes to incoming and outgoing archives. For more information, see <a href="https://msdn.microsoft.com/a02d2bc4-bbee-4eb5-8e19-6032957155ce">Registering for Event Notifications</a>.

The <b>IFaxServerNotify2</b> interface supports all the same methods as the <a href="https://msdn.microsoft.com/e8192f70-b0aa-4055-b67b-ff95991b66f2">IFaxServerNotify</a> interface and the additional method <a href="https://msdn.microsoft.com/4c768e39-9840-49be-b797-6150d53194bf">OnGeneralServerConfigChanged</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxServerNotify2</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFaxServerNotify2</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/9a5bdd1c-4583-4f79-9771-e377b52f888e">OnActivityLoggingConfigChange</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/9a5bdd1c-4583-4f79-9771-e377b52f888e">IFaxServerNotify2::OnActivityLoggingConfigChange</a> method when there is a configuration change related to activity logging.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9f5628e3-c6cf-4ee6-9a48-772403f57f37">OnDevicesConfigChange</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/9f5628e3-c6cf-4ee6-9a48-772403f57f37">IFaxServerNotify2::OnDevicesConfigChange</a> method when there is a change to a fax device configuration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5accf1c8-2047-4a30-bdc7-be99ddb728ce">OnDeviceStatusChange</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/5accf1c8-2047-4a30-bdc7-be99ddb728ce">IFaxServerNotify2::OnDeviceStatusChange</a> method when there is a change to a fax device status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d145cf69-16b4-415a-97b7-3661f72d5bb0">OnEventLoggingConfigChange</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/d145cf69-16b4-415a-97b7-3661f72d5bb0">IFaxServerNotify2::OnEventLoggingConfigChange</a> method when there is a configuration change related to event logging.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4c768e39-9840-49be-b797-6150d53194bf">OnGeneralServerConfigChanged</a>
</td>
<td align="left" width="63%">
Called by the fax service when the <a href="https://msdn.microsoft.com/4f492e5d-2ff2-445a-9f74-f83d96292403">IFaxServer2::Configuration</a> property changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b99c422f-6818-4e3a-ad24-b76d44efd64b">OnIncomingArchiveConfigChange</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/b99c422f-6818-4e3a-ad24-b76d44efd64b">IFaxServerNotify2::OnIncomingArchiveConfigChange</a> method when there is a configuration change related to the incoming fax archive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d109d2a9-a087-49de-bc89-cf62a664b23a">OnIncomingJobAdded</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/d109d2a9-a087-49de-bc89-cf62a664b23a">IFaxServerNotify2::OnIncomingJobAdded</a> method when an incoming fax job is added to the job queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/95a344c9-530b-435f-ad46-18ab93f0605f">OnIncomingJobChanged</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/95a344c9-530b-435f-ad46-18ab93f0605f">IFaxServerNotify2::OnIncomingJobChanged</a> method when the status of an incoming fax job changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e0d88299-bfee-4f83-883b-0e4b2acd8572">OnIncomingJobRemoved</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/e0d88299-bfee-4f83-883b-0e4b2acd8572">IFaxServerNotify2::OnIncomingJobRemoved</a> method when an incoming fax job is removed from the job queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d373c9bd-c57c-4197-8d46-42cb44fc73a5">OnIncomingMessageAdded</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/d373c9bd-c57c-4197-8d46-42cb44fc73a5">IFaxServerNotify2::OnIncomingMessageAdded</a> method when an incoming message is added to the inbound fax archive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/44a24087-246e-4d09-b3c7-afe644602376">OnIncomingMessageRemoved</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/44a24087-246e-4d09-b3c7-afe644602376">IFaxServerNotify2::OnIncomingMessageRemoved</a> method when an incoming message is removed from the inbound fax archive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/706784c1-cecf-477c-bd0e-094ffc1ad096">OnNewCall</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/706784c1-cecf-477c-bd0e-094ffc1ad096">IFaxServerNotify2::OnNewCall</a> method when there is a new incoming fax call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d726b6af-b8ec-4ab9-b0de-a6bf2305f429">OnOutboundRoutingGroupsConfigChange</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/d726b6af-b8ec-4ab9-b0de-a6bf2305f429">IFaxServerNotify2::OnOutboundRoutingGroupsConfigChange</a> method when there is a configuration change related to outbound fax routing groups.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0205cf78-f5cc-424c-b359-46f158e20f66">OnOutboundRoutingRulesConfigChange</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/0205cf78-f5cc-424c-b359-46f158e20f66">IFaxServerNotify2::OnOutboundRoutingRulesConfigChange</a> method when there is a configuration change related to outbound fax routing rules.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6c8e8873-8efc-4ba2-a4a3-c19a67d040fd">OnOutgoingArchiveConfigChange</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/6c8e8873-8efc-4ba2-a4a3-c19a67d040fd">IFaxServerNotify2::OnOutgoingArchiveConfigChange</a> method when there is a configuration change related to the outgoing fax archive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bc6a509b-8a8f-489a-b102-f9acb00dfb8e">OnOutgoingJobAdded</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/bc6a509b-8a8f-489a-b102-f9acb00dfb8e">IFaxServerNotify2::OnOutgoingJobAdded</a> method when an outgoing fax job is added to the job queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/95da9abe-497f-4ee5-b24c-2c74db71f634">OnOutgoingJobChanged</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/95da9abe-497f-4ee5-b24c-2c74db71f634">IFaxServerNotify2::OnOutgoingJobChanged</a> method when the status of an outgoing fax job changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/977e7a4c-0696-404c-90a7-8ef8147c3159">OnOutgoingJobRemoved</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/977e7a4c-0696-404c-90a7-8ef8147c3159">IFaxServerNotify2::OnOutgoingJobRemoved</a> method when an outgoing fax job is removed from the job queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1b5fcbb0-d6c4-43e4-88ff-4a9dd9af24f5">OnOutgoingMessageAdded</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/1b5fcbb0-d6c4-43e4-88ff-4a9dd9af24f5">IFaxServerNotify2::OnOutgoingMessageAdded</a> method when an outgoing message is added to the outbound fax archive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5bd6741a-9ca9-413e-bbda-674a398a3c0b">OnOutgoingMessageRemoved</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/5bd6741a-9ca9-413e-bbda-674a398a3c0b">IFaxServerNotify2::OnOutgoingMessageRemoved</a> method when an outgoing message is removed from the fax outbound archive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0c575631-8ce8-4e51-b640-a32f5b66d148">OnOutgoingQueueConfigChange</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/0c575631-8ce8-4e51-b640-a32f5b66d148">IFaxServerNotify2::OnOutgoingQueueConfigChange</a> method when there is a configuration change related to the outgoing fax job queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6d311077-7fae-4a32-89bf-1a4c66ea6b5e">OnQueuesStatusChange</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/6d311077-7fae-4a32-89bf-1a4c66ea6b5e">IFaxServerNotify2::OnQueuesStatusChange</a> method when there is a change in the fax job queue status.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3bcb2632-8ecf-4bc5-a130-94f8ea3a601a">OnReceiptOptionsChange</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/3bcb2632-8ecf-4bc5-a130-94f8ea3a601a">IFaxServerNotify2::OnReceiptOptionsChange</a> method when there is a change that relates to receipt configuration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f76d8702-42ba-4db2-b2e8-123f20ff876b">OnSecurityConfigChange</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/f76d8702-42ba-4db2-b2e8-123f20ff876b">IFaxServerNotify2::OnSecurityConfigChange</a> method when there is a configuration change related to security.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d61602b6-1f3d-46fc-b785-42d904927afe">OnServerActivityChange</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/d61602b6-1f3d-46fc-b785-42d904927afe">IFaxServerNotify2::OnServerActivityChange</a> method when the fax service activity and status changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7ed8ff7a-d54e-487e-8618-0ee8b284d4a3">OnServerShutDown</a>
</td>
<td align="left" width="63%">
The fax service calls the <a href="https://msdn.microsoft.com/7ed8ff7a-d54e-487e-8618-0ee8b284d4a3">IFaxServerNotify2::OnServerShutDown</a> method when the fax service shuts down.

</td>
</tr>
</table> 


## -remarks



<h3><a id="To_Use_Fax_Notification_Events_with_Visual_Basic"></a><a id="to_use_fax_notification_events_with_visual_basic"></a><a id="TO_USE_FAX_NOTIFICATION_EVENTS_WITH_VISUAL_BASIC"></a>To Use Fax Notification Events with Visual Basic</h3>
Use the following syntax when creating the root FaxServer2 object:


<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
Dim WithEvents objFaxServer2 As FaxServer2
</pre>
</td>
</tr>
</table></span></div>


For an example, see <a href="https://msdn.microsoft.com/3a9f42fa-383a-4072-92a6-b59f7940ab04">Registering for Fax Events</a>.
            

<h3><a id="To_Use_Fax_Notification_Events_with_C__"></a><a id="to_use_fax_notification_events_with_c__"></a><a id="TO_USE_FAX_NOTIFICATION_EVENTS_WITH_C__"></a>To Use Fax Notification Events with C++</h3>
A fax client application must implement <b>IFaxServerNotify2</b> and pass the fax service the pointer to an <b>IFaxServerNotify2</b> interface.
            



