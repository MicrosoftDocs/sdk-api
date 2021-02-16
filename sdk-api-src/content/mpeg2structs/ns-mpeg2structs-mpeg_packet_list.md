---
UID: NS:mpeg2structs.__MIDL___MIDL_itf_mpeg2structs_0000_0000_0015
title: MPEG_PACKET_LIST (mpeg2structs.h)
description: The MPEG_PACKET_LIST structure contains a list of MPEG-2 sections.
helpviewer_keywords: ["*PMPEG_PACKET_LIST","MPEG_PACKET_LIST","MPEG_PACKET_LIST structure [Microsoft TV Technologies]","PMPEG_PACKET_LIST","PMPEG_PACKET_LIST structure pointer [Microsoft TV Technologies]","mpeg2structs/MPEG_PACKET_LIST","mpeg2structs/PMPEG_PACKET_LIST","mstv.mpeg_packet_list"]
old-location: mstv\mpeg_packet_list.htm
tech.root: mstv
ms.assetid: 83131e71-3e06-4d42-9f71-f2da95400b63
ms.date: 12/05/2018
ms.keywords: '*PMPEG_PACKET_LIST, MPEG_PACKET_LIST, MPEG_PACKET_LIST structure [Microsoft TV Technologies], PMPEG_PACKET_LIST, PMPEG_PACKET_LIST structure pointer [Microsoft TV Technologies], mpeg2structs/MPEG_PACKET_LIST, mpeg2structs/PMPEG_PACKET_LIST, mstv.mpeg_packet_list'
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
req.typenames: MPEG_PACKET_LIST, *PMPEG_PACKET_LIST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_mpeg2structs_0000_0000_0015
 - mpeg2structs/__MIDL___MIDL_itf_mpeg2structs_0000_0000_0015
 - PMPEG_PACKET_LIST
 - mpeg2structs/PMPEG_PACKET_LIST
 - MPEG_PACKET_LIST
 - mpeg2structs/MPEG_PACKET_LIST
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
 - MPEG_PACKET_LIST
---

# MPEG_PACKET_LIST structure


## -description

The <b>MPEG_PACKET_LIST</b> structure contains a list of MPEG-2 sections.

## -struct-fields

### -field wPacketCount

Specifies the size of the <b>PacketList</b> array.

### -field PacketList

Specifies a pointer to an array of <a href="/previous-versions/windows/desktop/api/mpeg2structs/ns-mpeg2structs-mpeg_rqst_packet">MPEG_RQST_PACKET</a> structures, which themselves contain pointers to buffers that hold the sectioned data.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-structures">BDA Structures</a>



<a href="/previous-versions/windows/desktop/api/mpeg2structs/ns-mpeg2structs-mpeg_stream_buffer">MPEG_STREAM_BUFFER Structure</a>