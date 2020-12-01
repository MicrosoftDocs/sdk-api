---
UID: NN:rdpencomapi.IRDPSRAPISharingSession
title: IRDPSRAPISharingSession (rdpencomapi.h)
description: The main object that an application must create to start a collaboration session.
helpviewer_keywords: ["IRDPSRAPISharingSession","IRDPSRAPISharingSession interface [RDP]","IRDPSRAPISharingSession interface [RDP]","described","rdp.irdpsrapisharingsession","rdpencomapi/IRDPSRAPISharingSession"]
old-location: rdp\irdpsrapisharingsession.htm
tech.root: rdp
ms.assetid: 531382ec-d94f-411e-bd43-86cd3066ac26
ms.date: 12/05/2018
ms.keywords: IRDPSRAPISharingSession, IRDPSRAPISharingSession interface [RDP], IRDPSRAPISharingSession interface [RDP],described, rdp.irdpsrapisharingsession, rdpencomapi/IRDPSRAPISharingSession
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRDPSRAPISharingSession
 - rdpencomapi/IRDPSRAPISharingSession
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RdpEncom.dll
api_name:
 - IRDPSRAPISharingSession
---

# IRDPSRAPISharingSession interface


## -description

The main object that an application must create  to start a collaboration session. It is also the only object that you can create an instance of. The rest of the objects are accessed as session object properties.

The session object is hosted in-process by RdpEncom.dll. Even if the object is hosted in-process, there can be only one instance of this object created within a Winlogon session. Creating a second object will fail.

This interface uses the  single-threaded apartment (STA) threading model.
The object exposes a source interface that is used for firing session-specific events (<a href="/windows/win32/api/rdpencomapi/nn-rdpencomapi-_irdpsessionevents">_IRDPSessionEvents</a>) and a dual interface that is used for managing a session.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRDPSRAPISharingSession</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IRDPSRAPISharingSession</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IRDPSRAPISharingSession</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapisharingsession-close">Close</a>
</td>
<td align="left" width="63%">
Puts the session in an inactive state, closes all attendees, and stops listening to new incoming connections.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapisharingsession-connecttoclient">ConnectToClient</a>
</td>
<td align="left" width="63%">
Connects the viewer from the sharer in reverse connect mode if the viewer cannot connect to the sharer because of a network issue. For example, the viewer may not be able to connect to the sharer because of network address translation (NAT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapisharingsession-getdesktopsharedrect">GetDesktopSharedRect</a>
</td>
<td align="left" width="63%">
Retrieves the rectangle of the sharer's virtual desktop.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapisharingsession-open">Open</a>
</td>
<td align="left" width="63%">
Puts the session in an active state and starts listening to incoming connections.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapisharingsession-pause">Pause</a>
</td>
<td align="left" width="63%">
Pauses the encoding of the sharer's desktop  to pause sending graphics updates to all viewers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapisharingsession-resume">Resume</a>
</td>
<td align="left" width="63%">
Resumes the encoding of the sharer's desktop  to resume sending graphics updates to all viewers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapisharingsession-setdesktopsharedrect">SetDesktopSharedRect</a>
</td>
<td align="left" width="63%">
Sets the rectangle of the sharer's virtual desktop to be shared.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRDPSRAPISharingSession</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapisharingsession-get_applicationfilter">ApplicationFilter</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
An object implementing the <a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapiapplicationfilter">IRDPSRAPIApplicationFilter</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapisharingsession-get_attendees">Attendees</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
An object implementing the <a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapiattendeemanager">IRDPSRAPIAttendeeManager</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapisharingsession-get_colordepth">ColorDepth</a>


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

<a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapisharingsession-get_invitations">Invitations</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
An object implementing the <a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapiinvitationmanager">IRDPSRAPIInvitationManager</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapisharingsession-get_properties">Properties</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
An object implementing the <a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapisessionproperties">IRDPSRAPISessionProperties</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapisharingsession-get_virtualchannelmanager">VirtualChannelManager</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
An object implementing the <a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapivirtualchannelmanager">IRDPSRAPIVirtualChannelManager</a> interface.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapisharingsession2">IRDPSRAPISharingSession2</a>