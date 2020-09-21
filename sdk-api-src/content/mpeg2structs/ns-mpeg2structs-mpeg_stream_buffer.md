---
UID: NS:mpeg2structs.__MIDL___MIDL_itf_mpeg2structs_0000_0000_0023
title: MPEG_STREAM_BUFFER (mpeg2structs.h)
description: The MPEG_STREAM_BUFFER structure defines a buffer that receives MPEG-2 data.
helpviewer_keywords: ["*PMPEG_STREAM_BUFFER","MPEG_STREAM_BUFFER","MPEG_STREAM_BUFFER structure [Microsoft TV Technologies]","PMPEG_STREAM_BUFFER","PMPEG_STREAM_BUFFER structure pointer [Microsoft TV Technologies]","mpeg2structs/MPEG_STREAM_BUFFER","mpeg2structs/PMPEG_STREAM_BUFFER","mstv.mpeg_stream_buffer"]
old-location: mstv\mpeg_stream_buffer.htm
tech.root: mstv
ms.assetid: d376af4c-4b22-4a2d-917a-6f25d2c38861
ms.date: 12/05/2018
ms.keywords: '*PMPEG_STREAM_BUFFER, MPEG_STREAM_BUFFER, MPEG_STREAM_BUFFER structure [Microsoft TV Technologies], PMPEG_STREAM_BUFFER, PMPEG_STREAM_BUFFER structure pointer [Microsoft TV Technologies], mpeg2structs/MPEG_STREAM_BUFFER, mpeg2structs/PMPEG_STREAM_BUFFER, mstv.mpeg_stream_buffer'
req.header: mpeg2structs.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MPEG_STREAM_BUFFER, *PMPEG_STREAM_BUFFER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_mpeg2structs_0000_0000_0023
 - mpeg2structs/__MIDL___MIDL_itf_mpeg2structs_0000_0000_0023
 - PMPEG_STREAM_BUFFER
 - mpeg2structs/PMPEG_STREAM_BUFFER
 - MPEG_STREAM_BUFFER
 - mpeg2structs/MPEG_STREAM_BUFFER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mpeg2Structs.h
api_name:
 - MPEG_STREAM_BUFFER
---

# MPEG_STREAM_BUFFER structure


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

This structure is used with the <a href="/previous-versions/windows/desktop/api/mpeg2data/nf-mpeg2data-impeg2stream-supplydatabuffer">IMpeg2Stream::SupplyDataBuffer</a> method to get raw MPEG-2 data.

For PSI tables and sections, set <b>pDataBuffer</b> to point to a <a href="/previous-versions/windows/desktop/api/mpeg2structs/ns-mpeg2structs-section">SECTION</a> structure. If you also create an <a href="/previous-versions/windows/desktop/api/mpeg2structs/ns-mpeg2structs-mpeg_packet_list">MPEG_PACKET_LIST</a> structure to hold a list of buffers, you can pass that list to the <a href="/previous-versions/windows/desktop/api/mpeg2data/nf-mpeg2data-isectionlist-initializewithrawsections">ISectionList::InitializeWithRawSections</a> method.


#### Examples

The following code shows how to initialize an <b>MPEG_STREAM_BUFFER</b> structure so that it points to a <b>SECTION</b> structure contained in an <b>MPEG_PACKET_LIST</b> section list:


```cpp

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
Packets.PacketList[0] = &RqstPacket[0];
Packets.PacketList[1] = &RqstPacket[1];

// Set the stream buffer structure to point to the first packet in the list.
MPEG_STREAM_BUFFER StreamBuffer;
ZeroMemory(&StreamBuffer, sizeof(MPEG_STREAM_BUFFER));
StreamBuffer.dwDataBufferSize = Packets.PacketList[0]->dwLength;
StreamBuffer.pDataBuffer = (BYTE*) Packets.PacketList[0]->pSection;

```

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-structures">BDA Structures</a>