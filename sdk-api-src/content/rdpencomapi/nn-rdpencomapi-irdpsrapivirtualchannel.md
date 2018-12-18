---
UID: NN:rdpencomapi.IRDPSRAPIVirtualChannel
title: IRDPSRAPIVirtualChannel
author: windows-sdk-content
description: Manages the virtual channel.
old-location: rdp\irdpsrapivirtualchannel.htm
tech.root: rdp
ms.assetid: c3cceb22-424d-4ed9-8d4d-0ca523ba5e9c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IRDPSRAPIVirtualChannel, IRDPSRAPIVirtualChannel interface [RDP], IRDPSRAPIVirtualChannel interface [RDP],described, rdp.irdpsrapivirtualchannel, rdpencomapi/IRDPSRAPIVirtualChannel
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
 - IRDPSRAPIVirtualChannel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRDPSRAPIVirtualChannel interface


## -description


Manages the virtual channel.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRDPSRAPIVirtualChannel</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IRDPSRAPIVirtualChannel</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IRDPSRAPIVirtualChannel</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d861de01-70e3-49b0-91b3-01f6b0051823">SendData</a>
</td>
<td align="left" width="63%">
Sends data on the channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7d4a19d3-b089-4689-9062-a5b52251776f">SetAccess</a>
</td>
<td align="left" width="63%">
Enables the channel for an attendee.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRDPSRAPIVirtualChannel</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/a6c75a09-f791-4dca-8059-33f03b4e3d1e">Flags</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The channel flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/0676cdb0-87af-4e4d-86b5-b5b235a94d3f">Name</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The channel name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/34addc3d-5541-48c9-a749-256114e0c2aa">Priority</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The channel priority.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/750e7d98-196f-4bf2-864b-50b3bef6f6ad">IRDPSRAPIVirtualChannelManager</a>
 

 

