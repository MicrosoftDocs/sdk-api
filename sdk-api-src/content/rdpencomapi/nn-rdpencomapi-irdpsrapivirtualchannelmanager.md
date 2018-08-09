---
UID: NN:rdpencomapi.IRDPSRAPIVirtualChannelManager
title: IRDPSRAPIVirtualChannelManager
author: windows-sdk-content
description: Manages the list of virtual channels.
old-location: rdp\irdpsrapivirtualchannelmanager.htm
old-project: rdp
ms.assetid: 750e7d98-196f-4bf2-864b-50b3bef6f6ad
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IRDPSRAPIVirtualChannelManager, IRDPSRAPIVirtualChannelManager interface [RDP], IRDPSRAPIVirtualChannelManager interface [RDP],described, rdp.irdpsrapivirtualchannelmanager, rdpencomapi/IRDPSRAPIVirtualChannelManager
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: RDPENCOMAPI_CONSTANTS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RdpEncom.dll
api_name:
 - IRDPSRAPIVirtualChannelManager
product: Windows
targetos: Windows
req.lib: 
req.dll: RdpEncom.dll
req.irql: 
req.product: ADAM
---

# IRDPSRAPIVirtualChannelManager interface


## -description


Manages the list of virtual channels.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRDPSRAPIVirtualChannelManager</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IRDPSRAPIVirtualChannelManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IRDPSRAPIVirtualChannelManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0185af26-a29d-4227-bad6-2633de18617e">CreateVirtualChannel</a>
</td>
<td align="left" width="63%">
Creates a virtual channel.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRDPSRAPIVirtualChannelManager</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh439300">_NewEnum</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
An enumerator interface for the virtual channel collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh451057">Item</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
An item in the virtual channel collection.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/c3cceb22-424d-4ed9-8d4d-0ca523ba5e9c">IRDPSRAPIVirtualChannel</a>
 

 

