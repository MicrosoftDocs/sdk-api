---
UID: NS:bdatypes._MPEG2_TRANSPORT_STRIDE
title: "_MPEG2_TRANSPORT_STRIDE"
author: windows-driver-content
description: The MPEG2_TRANSPORT_STRIDE structure describes the format of MPEG-2 transport stream (TS) packets.
old-location: dshow\mpeg2_transport_stride.htm
old-project: DirectShow
ms.assetid: 269d5fba-2dea-4786-93d6-e52b56c8bb53
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: "*PMPEG2_TRANSPORT_STRIDE, MPEG2_TRANSPORT_STRIDE, MPEG2_TRANSPORT_STRIDE structure [DirectShow], PMPEG2_TRANSPORT_STRIDE, PMPEG2_TRANSPORT_STRIDE structure pointer [DirectShow], _MPEG2_TRANSPORT_STRIDE, bdatypes/MPEG2_TRANSPORT_STRIDE, bdatypes/PMPEG2_TRANSPORT_STRIDE, dshow.mpeg2_transport_stride"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: bdatypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MPEG2_TRANSPORT_STRIDE, *PMPEG2_TRANSPORT_STRIDE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	bdatypes.h
api_name:
-	MPEG2_TRANSPORT_STRIDE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _MPEG2_TRANSPORT_STRIDE structure


## -description



The <code>MPEG2_TRANSPORT_STRIDE</code> structure describes the format of MPEG-2 transport stream (TS) packets. This structure allows for transports streams in which the 188-byte transport packets are not contiguous. For the purpose of this documentation, such packets are referred to as <i>stride packets</i>.

Stride packets are identified by the following media type:

<table>
<tr>
<td>Major Type</td>
<td>MEDIATYPE_Stream</td>
</tr>
<tr>
<td>Subtype</td>
<td>MEDIASUBTYPE_MPEG2_TRANSPORT_STRIDE</td>
</tr>
<tr>
<td>Format Type</td>
<td>FORMAT_None</td>
</tr>
</table>
 

The format block (<b>pbFormat</b>) is optional. If the format block is included, it must begin with an <b>MPEG2_TRANSPORT_STRIDE</b> structure. This structure defines the layout of the transport packet within the stride packet. If the format block is <b>NULL</b>, the packets are assumed to use a set of default values; see the Remarks section for details.




## -struct-fields




### -field dwOffset

Specifies the offset, in bytes, from the beginning of the packet to the first byte of the embedded transport packet. The value must range from zero to <code>(dwStride - dwPacketLength)</code>, inclusive.


### -field dwPacketLength

Specifies the length of the embedded transport packet, in bytes. For standard MPEG-2 transport packets, the value must be 188 bytes.


### -field dwStride

Specifies the length of the entire stride packet, in bytes. The value must be at least <code>(dwOffset + dwPacketLength)</code>.


## -remarks



The following diagram illustrates the relations between the structure members.

<img alt="MPEG-2 stride packet" border="0" src="images/mpeg2_stride_packet.png"/>

Input buffers that contain multiplexed stride packets have some restrictions:

<ul>
<li>Stride packets must be packed contiguously within the buffer.</li>
<li>No bytes may precede the first stride packet or follow the last stride packet.</li>
<li>An integral number of stride packets must fit in the buffer; that is, buffer length % dwStride equals zero.</li>
</ul>
There is no restriction on the number of stride packets per buffer.

If the media type does not contain a format block (<b>pbFormat</b> is <b>NULL</b>), the following default values are used:

<ul>
<li><b>dwOffset</b>: 0</li>
<li><b>dwPacketLength</b>: 188</li>
<li><b>dwStride</b>: 188</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>



<a href="https://msdn.microsoft.com/20fb2dc3-76b5-421a-b8e1-d99fad2ce2dd">MPEG-2 Media Types</a>
 

 

