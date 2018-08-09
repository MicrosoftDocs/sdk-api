---
UID: NN:rdpencomapi.IRDPSRAPIFrameBuffer
title: IRDPSRAPIFrameBuffer
author: windows-sdk-content
description: Provides data about the frame buffer size and format and allows the contents to be retrieved.
old-location: rdp\irdpsrapiframebuffer.htm
old-project: rdp
ms.assetid: ab40bdd2-448f-4867-aabd-d6b66add5247
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IRDPSRAPIFrameBuffer, IRDPSRAPIFrameBuffer interface [RDP], IRDPSRAPIFrameBuffer interface [RDP],described, rdp.irdpsrapiframebuffer, rdpencomapi/IRDPSRAPIFrameBuffer
ms.prod: windows
ms.technology: windows-sdk
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
 - IRDPSRAPIFrameBuffer
product: Windows
targetos: Windows
req.lib: 
req.dll: RdpEncom.dll
req.irql: 
req.product: ADAM
---

# IRDPSRAPIFrameBuffer interface


## -description


Provides data about the frame buffer size and format and allows the contents to be retrieved.

Applications can get a pointer to this interface from the <b>FrameBuffer</b> property of the <a href="https://msdn.microsoft.com/3ac68be7-e6fd-42c7-b2f3-b90bb5097b07">IRDPSRAPISharingSession2</a> interface. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRDPSRAPIFrameBuffer</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IRDPSRAPIFrameBuffer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IRDPSRAPIFrameBuffer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6497d9d1-c987-40ea-b384-0fff1e852122">GetFrameBufferBits</a>
</td>
<td align="left" width="63%">
Gets a specified area of the frame buffer.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRDPSRAPIFrameBuffer</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/864e7669-fc33-4473-9106-d436d6900bf2">Bpp</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Bits per pixel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/ff542686">Height</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The height of the frame in pixels.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/ff553316">Width</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The width of the frame in pixels.

</td>
</tr>
</table> 

