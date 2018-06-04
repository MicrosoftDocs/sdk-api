---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# __MIDL___MIDL_itf_mpeg2structs_0000_0000_0023 structure


## -description



The <b>MPEG_STREAM_BUFFER</b> structure defines a buffer that receives MPEG-2 data.




## -struct-fields




### -field hr

Specifies a status code. Use this value to check the status of the read request.


### -field dwDataBufferSize

Specifies the size of the buffer, in bytes.


### -field dwSizeOfDataRead

Specifies the amount of valid data in the buffer, in bytes


### -field pDataBuffer

Pointer to a buffer that holds the MPEG-2 data.


## -remarks



This structure is used with the <a href="https://msdn.microsoft.com/68950eba-6c23-49f7-9651-d4db9e554de3">IMpeg2Stream::SupplyDataBuffer</a> method to get raw MPEG-2 data.

For PSI tables and sections, set <b>pDataBuffer</b> to point to a <a href="https://msdn.microsoft.com/6ee07b84-ae97-413f-a3b4-0078ad740194">SECTION</a> structure. If you also create an <a href="https://msdn.microsoft.com/83131e71-3e06-4d42-9f71-f2da95400b63">MPEG_PACKET_LIST</a> structure to hold a list of buffers, you can pass that list to the <a href="https://msdn.microsoft.com/61f1e99b-c375-4aa3-a11b-7e24c35f71ca">ISectionList::InitializeWithRawSections</a> method.


#### Examples

The following code shows how to initialize an <b>MPEG_STREAM_BUFFER</b> structure so that it points to a <b>SECTION</b> structure contained in an <b>MPEG_PACKET_LIST</b> section list:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
// Allocate two buffers for section data.
const int cBufferSize = 4096;
BYTE pBuffer1[cBufferSize];
BYTE pBuffer2[cBufferSize];

// Create a packet list to hold both buffers.
MPEG_RQST_PACKET RqstPacket[2];
MPEG_PACKET_LIST Packets;

RqstPacket[0].dwLength = cBufferSize;
RqstPacket[0].pSection = (SECTION*)pBuffer1;
RqstPacket[1].dwLength = cBufferSize;
RqstPacket[1].pSection = (SECTION*)pBuffer2;

Packets.wPacketCount = 2;
Packets.PacketList[0] = &amp;RqstPacket[0];
Packets.PacketList[1] = &amp;RqstPacket[1];

// Set the stream buffer structure to point to the first packet in the list.
MPEG_STREAM_BUFFER StreamBuffer;
ZeroMemory(&amp;StreamBuffer, sizeof(MPEG_STREAM_BUFFER));
StreamBuffer.dwDataBufferSize = Packets.PacketList[0]-&gt;dwLength;
StreamBuffer.pDataBuffer = (BYTE*) Packets.PacketList[0]-&gt;pSection;
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/5ae43ac6-519d-486b-aaa5-c766f3194ef2">BDA Structures</a>
 

 

