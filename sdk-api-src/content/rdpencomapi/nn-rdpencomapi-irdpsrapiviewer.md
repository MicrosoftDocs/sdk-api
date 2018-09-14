---
UID: NN:rdpencomapi.IRDPSRAPIViewer
title: IRDPSRAPIViewer
author: windows-sdk-content
description: The ActiveX interface that is used on the viewer side.
old-location: rdp\irdpsrapiviewer.htm
tech.root: Rdp
ms.assetid: 6bafe380-2ef4-4e93-a6cd-143798437615
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IRDPSRAPIViewer, IRDPSRAPIViewer interface [RDP], IRDPSRAPIViewer interface [RDP],described, rdp.irdpsrapiviewer, rdpencomapi/IRDPSRAPIViewer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IRDPSRAPIViewer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRDPSRAPIViewer interface


## -description


<p class="CCE_Message">[The <b>IRDPSRAPIViewer</b> interface is no longer available for use for UWP applications as of Windows 10, version 1709. It is still supported for Desktop Apps.]

The ActiveX interface that is used on the viewer side.  The <b>IRDPSRAPIViewer</b> interface is equivalent to the <a href="https://msdn.microsoft.com/531382ec-d94f-411e-bd43-86cd3066ac26">IRDPSRAPISharingSession</a> interface on the sharer side.

This interface can be used to connect or  disconnect viewers and to get or set various properties on the viewer ActiveX control.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRDPSRAPIViewer</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IRDPSRAPIViewer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IRDPSRAPIViewer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f3deec96-af56-4ebe-a5c3-25a4c7be14c0">Connect</a>
</td>
<td align="left" width="63%">
Initiates a connection from the viewer to the sharer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/526b91aa-a5b9-4ee9-873f-ca23c4633d21">Disconnect</a>
</td>
<td align="left" width="63%">
Initiates a disconnect of the viewer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3dd57235-89bb-4199-a95a-d8f522cda6a2">RequestColorDepthChange</a>
</td>
<td align="left" width="63%">
Requests a change of color depth on the sharer Winlogon session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/be913f3c-9a5b-46bd-be9a-1ba0b0c20211">RequestControl</a>
</td>
<td align="left" width="63%">
Requests a control level change.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6e45e21f-f3a5-4a9e-9d63-45d7a1972114">StartReverseConnectListener</a>
</td>
<td align="left" width="63%">
Initiates a reverse connection listener for listening connections from the sharer.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRDPSRAPIViewer</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/984c7238-99ba-438f-b122-e952f95e018d">ApplicationFilter</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
An application filter object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7d61577b-d8e3-49d9-ac61-cc7c35cdd87f">Attendees</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
An attendee list object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/010974ee-d5b0-436d-9553-18ae62d09bf2">DisconnectedText</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The text that will be displayed in the control in disconnected mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/2657e79a-de3a-44e1-90af-81242ac123f6">Invitations</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
An invitation list object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/86930ad8-6389-47b9-9397-0662a0a36f04">Properties</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
A property list object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/3de98656-7d66-4d39-a5a7-a8240553c72f">SmartSizing</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The smart sizing property of the ActiveX control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/c878c445-5f1a-4a1f-be56-4cc427a40a1a">VirtualChannelManager</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
A virtual channel manager object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>
 

 

