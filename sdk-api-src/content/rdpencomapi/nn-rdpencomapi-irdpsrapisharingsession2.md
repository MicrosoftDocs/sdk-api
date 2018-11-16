---
UID: NN:rdpencomapi.IRDPSRAPISharingSession2
title: IRDPSRAPISharingSession2
author: windows-sdk-content
description: The main object that an application must create to start a collaboration session.
old-location: rdp\irdpsrapisharingsession2.htm
tech.root: Rdp
ms.assetid: 3ac68be7-e6fd-42c7-b2f3-b90bb5097b07
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IRDPSRAPISharingSession2, IRDPSRAPISharingSession2 interface [RDP], IRDPSRAPISharingSession2 interface [RDP],described, rdp.irdpsrapisharingsession2, rdpencomapi/IRDPSRAPISharingSession2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
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
 - IRDPSRAPISharingSession2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRDPSRAPISharingSession2 interface


## -description


The main object that an application must create  to start a collaboration session. The 
    session object is hosted in-process by RdpEncom.dll. Even though session object is hosted in-process, 
    there can be only one instance of this object created within a Winlogon session. Creating a second object will 
    fail.

This interface uses the  single-threaded apartment (STA) threading model. The object exposes a source interface 
    that is used for firing session-specific events 
    (<a href="https://msdn.microsoft.com/89ffdf37-156f-4977-93c4-bf9fe5aec838">_IRDPSessionEvents</a>) and a dual interface that is used 
    for managing a session.

This interface extends the 
    <a href="https://msdn.microsoft.com/531382ec-d94f-411e-bd43-86cd3066ac26">IRDPSRAPISharingSession</a> interface and contains the 
    following members.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRDPSRAPISharingSession2</b> interface inherits from <a href="https://msdn.microsoft.com/531382ec-d94f-411e-bd43-86cd3066ac26">IRDPSRAPISharingSession</a>. <b>IRDPSRAPISharingSession2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IRDPSRAPISharingSession2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ab6e27d8-b6f2-42a6-a0f6-cfdfb5ec9a13">Close</a>
</td>
<td align="left" width="63%">
Puts the session in an inactive state, closes all attendees, and stops listening to new incoming connections.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/18651433-90cb-4ebd-afaf-480800dfe033">ConnectToClient</a>
</td>
<td align="left" width="63%">
Connects the viewer from the sharer in reverse connect mode if the viewer cannot connect to the sharer because of a network issue. For example, the viewer may not be able to connect to the sharer because of network address translation (NAT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/78f517c9-0870-4dfd-a318-3bd510e05dfa">ConnectUsingTransportStream</a>
</td>
<td align="left" width="63%">
Connects using the specified transport stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b224fa2-928d-4222-80a6-91f654b97ae1">GetDesktopSharedRect</a>
</td>
<td align="left" width="63%">
Retrieves the rectangle of the sharer's virtual desktop.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2c97a37d-5862-4ad3-9029-481ea0a789e0">Open</a>
</td>
<td align="left" width="63%">
Puts the session in an active state and starts listening to incoming connections.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1ea0e8c4-39ef-4261-af7b-d27d6052c17d">Pause</a>
</td>
<td align="left" width="63%">
Pauses the encoding of the sharer's desktop  to pause sending graphics updates to all viewers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3e99d514-a6fe-4855-99ab-9ab2b5cbcc9b">Resume</a>
</td>
<td align="left" width="63%">
Resumes the encoding of the sharer's desktop  to resume sending graphics updates to all viewers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d10c8f2b-b1ee-4966-9e96-21e78124874b">SendControlLevelChangeResponse</a>
</td>
<td align="left" width="63%">
Sends an <a href="https://msdn.microsoft.com/E190DAEC-776A-4248-8A73-073AB6F2FE8A">OnControlLevelChangeResponse</a> event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8dda8b52-5bec-45ed-9215-2009cb74bf3e">SetDesktopSharedRect</a>
</td>
<td align="left" width="63%">
Sets the rectangle of the sharer's virtual desktop to be shared.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRDPSRAPISharingSession2</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/4a346305-972c-40c4-882e-905745edf6e9">ApplicationFilter</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
An object implementing the <a href="https://msdn.microsoft.com/6a08c948-1b25-4a36-93c8-23e7e3f4fb08">IRDPSRAPIApplicationFilter</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/bcbc8f16-855d-4835-966c-73773f3ac6d4">Attendees</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
An object implementing the <a href="https://msdn.microsoft.com/202b539c-b7a0-4cf3-ba64-f60cc062575a">IRDPSRAPIAttendeeManager</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8835a79c-281a-4f50-ba41-c9d4a0a8d7bd">ColorDepth</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The color depth of the session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/2547b317-0c1b-429c-81d4-7cb97e1cc3e0">FrameBuffer</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/ab40bdd2-448f-4867-aabd-d6b66add5247">IRDPSRAPIFrameBuffer</a> interface for the session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/6e5116d9-7b65-4d93-ab1e-caac080e870e">Invitations</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
An object implementing the <a href="https://msdn.microsoft.com/300940ef-e8a6-4dd9-a078-d4325e20ae91">IRDPSRAPIInvitationManager</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d9eff86e-74ee-440b-9f89-7cf26ba1ac39">Properties</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
An object implementing the <a href="https://msdn.microsoft.com/bf4d9df2-8436-4d21-9016-7db231212155">IRDPSRAPISessionProperties</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/ba951d8a-cf8e-4183-a40b-beba45fd48ef">VirtualChannelManager</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
An object implementing the <a href="https://msdn.microsoft.com/750e7d98-196f-4bf2-864b-50b3bef6f6ad">IRDPSRAPIVirtualChannelManager</a> interface.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/531382ec-d94f-411e-bd43-86cd3066ac26">IRDPSRAPISharingSession</a>
 

 

