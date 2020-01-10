---
UID: NN:rdpencomapi.IRDPSRAPIFrameBuffer
title: IRDPSRAPIFrameBuffer (rdpencomapi.h)
description: Provides data about the frame buffer size and format and allows the contents to be retrieved.
old-location: rdp\irdpsrapiframebuffer.htm
tech.root: rdp
ms.assetid: ab40bdd2-448f-4867-aabd-d6b66add5247
ms.date: 12/05/2018
ms.keywords: IRDPSRAPIFrameBuffer, IRDPSRAPIFrameBuffer interface [RDP], IRDPSRAPIFrameBuffer interface [RDP],described, rdp.irdpsrapiframebuffer, rdpencomapi/IRDPSRAPIFrameBuffer
f1_keywords:
- rdpencomapi/IRDPSRAPIFrameBuffer
dev_langs:
- c++
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
- IRDPSRAPIFrameBuffer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRDPSRAPIFrameBuffer interface


## -description


Provides data about the frame buffer size and format and allows the contents to be retrieved.

Applications can get a pointer to this interface from the <b>FrameBuffer</b> property of the <a href="https://docs.microsoft.com/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapisharingsession2">IRDPSRAPISharingSession2</a> interface. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRDPSRAPIFrameBuffer</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IRDPSRAPIFrameBuffer</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapiframebuffer-getframebufferbits">GetFrameBufferBits</a>
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

<a href="https://docs.microsoft.com/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapiframebuffer-get_bpp">Bpp</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapiframebuffer-get_height">Height</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapiframebuffer-get_width">Width</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The width of the frame in pixels.

</td>
</tr>
</table> 

