---
UID: NS:mpeg2structs.__MIDL___MIDL_itf_mpeg2structs_0000_0000_0015
title: "__MIDL___MIDL_itf_mpeg2structs_0000_0000_0015"
author: windows-sdk-content
description: The MPEG_PACKET_LIST structure contains a list of MPEG-2 sections.
old-location: mstv\mpeg_packet_list.htm
old-project: mstv
ms.assetid: 83131e71-3e06-4d42-9f71-f2da95400b63
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: "*PMPEG_PACKET_LIST, MPEG_PACKET_LIST, MPEG_PACKET_LIST structure [Microsoft TV Technologies], PMPEG_PACKET_LIST, PMPEG_PACKET_LIST structure pointer [Microsoft TV Technologies], __MIDL___MIDL_itf_mpeg2structs_0000_0000_0015, mpeg2structs/MPEG_PACKET_LIST, mpeg2structs/PMPEG_PACKET_LIST, mstv.mpeg_packet_list"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: mpeg2structs.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: MPEG_PACKET_LIST, *PMPEG_PACKET_LIST
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mpeg2Structs.h
api_name:
 - MPEG_PACKET_LIST
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# __MIDL___MIDL_itf_mpeg2structs_0000_0000_0015 structure


## -description



The <b>MPEG_PACKET_LIST</b> structure contains a list of MPEG-2 sections.




## -struct-fields




### -field wPacketCount

Specifies the size of the <b>PacketList</b> array.


### -field PacketList

Specifies a pointer to an array of <a href="https://msdn.microsoft.com/b7777633-66c3-44c2-9cdb-14c540555a43">MPEG_RQST_PACKET</a> structures, which themselves contain pointers to buffers that hold the sectioned data.


## -see-also




<a href="https://msdn.microsoft.com/5ae43ac6-519d-486b-aaa5-c766f3194ef2">BDA Structures</a>



<a href="https://msdn.microsoft.com/d376af4c-4b22-4a2d-917a-6f25d2c38861">MPEG_STREAM_BUFFER Structure</a>
 

 

