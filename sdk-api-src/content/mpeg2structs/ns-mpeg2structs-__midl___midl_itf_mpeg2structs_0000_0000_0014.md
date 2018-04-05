---
UID: NS:mpeg2structs.__MIDL___MIDL_itf_mpeg2structs_0000_0000_0014
title: "__MIDL___MIDL_itf_mpeg2structs_0000_0000_0014"
author: windows-driver-content
description: The MPEG_RQST_PACKET structure defines a buffer to receive MPEG-2 section data.
old-location: mstv\mpeg_rqst_packet.htm
old-project: mstv
ms.assetid: b7777633-66c3-44c2-9cdb-14c540555a43
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: "*PMPEG_RQST_PACKET, MPEG_RQST_PACKET, MPEG_RQST_PACKET structure [Microsoft TV Technologies], PMPEG_RQST_PACKET, PMPEG_RQST_PACKET structure pointer [Microsoft TV Technologies], __MIDL___MIDL_itf_mpeg2structs_0000_0000_0014, mpeg2structs/MPEG_RQST_PACKET, mpeg2structs/PMPEG_RQST_PACKET, mstv.mpeg_rqst_packet"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: MPEG_RQST_PACKET, *PMPEG_RQST_PACKET
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Mpeg2Structs.h
api_name:
-	MPEG_RQST_PACKET
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# __MIDL___MIDL_itf_mpeg2structs_0000_0000_0014 structure


## -description



The <b>MPEG_RQST_PACKET</b> structure defines a buffer to receive MPEG-2 section data.




## -struct-fields




### -field dwLength

Specifies the length of the buffer that <b>pSection</b> points to. The minimum size for section data is 4096 bytes.


### -field pSection

Pointer to a buffer that receives the section data. The pointer is typed as a <a href="https://msdn.microsoft.com/6ee07b84-ae97-413f-a3b4-0078ad740194">SECTION</a> structure. The first bytes in the section contain header fields that are defined in the <b>SECTION</b> structure. The <b>SectionData</b> member of the <b>SECTION</b> structure is an array of bytes, containing the body of the section after the header bytes.


## -see-also




<a href="https://msdn.microsoft.com/5ae43ac6-519d-486b-aaa5-c766f3194ef2">BDA Structures</a>



<a href="https://msdn.microsoft.com/83131e71-3e06-4d42-9f71-f2da95400b63">MPEG_PACKET_LIST Structure</a>
 

 

