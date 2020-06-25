---
UID: NN:rdpencomapi.IRDPSRAPIVirtualChannel
title: IRDPSRAPIVirtualChannel (rdpencomapi.h)
description: Manages the virtual channel.
helpviewer_keywords: ["IRDPSRAPIVirtualChannel","IRDPSRAPIVirtualChannel interface [RDP]","IRDPSRAPIVirtualChannel interface [RDP]","described","rdp.irdpsrapivirtualchannel","rdpencomapi/IRDPSRAPIVirtualChannel"]
old-location: rdp\irdpsrapivirtualchannel.htm
tech.root: rdp
ms.assetid: c3cceb22-424d-4ed9-8d4d-0ca523ba5e9c
ms.date: 12/05/2018
ms.keywords: IRDPSRAPIVirtualChannel, IRDPSRAPIVirtualChannel interface [RDP], IRDPSRAPIVirtualChannel interface [RDP],described, rdp.irdpsrapivirtualchannel, rdpencomapi/IRDPSRAPIVirtualChannel
f1_keywords:
- rdpencomapi/IRDPSRAPIVirtualChannel
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRDPSRAPIVirtualChannel interface


## -description


Manages the virtual channel.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRDPSRAPIVirtualChannel</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IRDPSRAPIVirtualChannel</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapivirtualchannel-senddata">SendData</a>
</td>
<td align="left" width="63%">
Sends data on the channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapivirtualchannel-setaccess">SetAccess</a>
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

<a href="https://docs.microsoft.com/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapivirtualchannel-get_flags">Flags</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapivirtualchannel-get_name">Name</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapivirtualchannel-get_priority">Priority</a>


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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapivirtualchannelmanager">IRDPSRAPIVirtualChannelManager</a>
 

 

