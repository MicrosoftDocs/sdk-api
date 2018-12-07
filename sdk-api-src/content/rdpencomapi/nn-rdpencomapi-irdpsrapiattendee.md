---
UID: NN:rdpencomapi.IRDPSRAPIAttendee
title: IRDPSRAPIAttendee
author: windows-sdk-content
description: Attendee objects are created as a result of clients connecting to the session and being authenticated. After an attendee object is created, it is automatically added to the attendees list.
old-location: rdp\irdpsrapiattendee.htm
tech.root: rdp
ms.assetid: e9edd9f2-ccbf-45b2-b71c-e30368435a60
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IRDPSRAPIAttendee, IRDPSRAPIAttendee interface [RDP], IRDPSRAPIAttendee interface [RDP],described, rdp.irdpsrapiattendee, rdpencomapi/IRDPSRAPIAttendee
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: RdpEncomAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: RdpEncomAPI.tlb
req.lib: 
req.dll: RdpEncom.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RdpEncom.dll
api_name:
 - IRDPSRAPIAttendee
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRDPSRAPIAttendee interface


## -description


Attendee objects are created as a result of clients connecting to the session and being authenticated. After an attendee object is created, it is automatically added to the attendees list.You cannot create an instance of this object. Applications can get access to attendee objects in the following ways:

<ul>
<li>When the <a href="https://msdn.microsoft.com/cf3c41c9-d572-433a-ba80-960d38296749">IRDPSessionEvents::OnAttendeeConnected</a> event is fired, the parameter is an <b>IDispatch</b> pointer corresponding to the attendee object that was created.</li>
<li>By accessing the Attendee property of the AttendeeDisconnectInfo object. An <b>IDispatch</b> pointer to this object is fired by the <a href="https://msdn.microsoft.com/4edcd497-8821-46c0-8d44-0b24e4f3f285">IRDPSessionEvents::OnAttendeeDisconnected</a> event. This is how applications are informed of what attendee was disconnected.</li>
<li>By calling the <a href="https://msdn.microsoft.com/963f795a-3da4-45d0-b609-8fcc2d6e5700">get_Item</a> method on the <a href="https://msdn.microsoft.com/202b539c-b7a0-4cf3-ba64-f60cc062575a">IRDPSRAPIAttendeeManager</a> interface.</li>
<li>By calling <b>get_Next</b> on the enumerator returned by the <a href="https://msdn.microsoft.com/f79bfd9c-b9f9-4da4-977c-cae8f11ba239">IRDPSRAPIAttendeeManager::get__NewEnum</a> method.</li>
</ul>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRDPSRAPIAttendee</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IRDPSRAPIAttendee</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IRDPSRAPIAttendee</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e666fdd4-7417-40ea-9643-d7df587294f2">TerminateConnection</a>
</td>
<td align="left" width="63%">
Disconnects the client represented by the attendee.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRDPSRAPIAttendee</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/40112da5-c7b6-42f9-9acf-887161aceabf">ConnectivityInfo</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The connectivity information for the attendee.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/b154580d-f541-4668-9255-607ab2de46a9">ControlLevel</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The level of control the attendee has over the session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e2e6bef1-6828-473c-aa33-ab30ebe56948">Flags</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The attendee specific flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9ed04c11-d3cc-4846-88e8-aad9fb23fee8">Id</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The unique identifier for the attendee.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/71fed876-8b9d-4b19-a278-45ab620fb61e">Invitation</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The invitation used to grant the attendee access to the conference.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/69861a6d-3dc5-4871-8e99-0d46d2896dcc">RemoteName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The name of the remote client. This is usually the attendee's friendly name.

</td>
</tr>
</table> 


## -remarks



Applications should not save pointers to attendee objects. The lifetime of the attendee object depends on the lifetime of the <b>RDPSession</b> object. It also depends if the session is still in the opened state and if the client corresponding to the attendee object is still connected to the session. Applications can keep references to attendee objects but calling some methods on it after the client disconnected or after the session is destroyed will return <b>E_UNEXPECTED</b> failures.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/849c4fbe-b9c4-4601-b93f-13efd1014a50">IRDPSRAPIAttendeeDisconnectInfo</a>



<a href="https://msdn.microsoft.com/202b539c-b7a0-4cf3-ba64-f60cc062575a">IRDPSRAPIAttendeeManager</a>
 

 

