---
UID: NE:mpeg2structs.__MIDL___MIDL_itf_mpeg2structs_0000_0000_0032
title: MPEG_REQUEST_TYPE (mpeg2structs.h)
description: The MPEG_REQUEST_TYPE enumeration type specifies a request for MPEG-2 data.
helpviewer_keywords: ["MPEG_REQUEST_TYPE","MPEG_REQUEST_TYPE enumeration [Microsoft TV Technologies]","MPEG_RQST_GET_PES_STREAM","MPEG_RQST_GET_SECTION","MPEG_RQST_GET_SECTIONS_STREAM","MPEG_RQST_GET_SECTION_ASYNC","MPEG_RQST_GET_TABLE","MPEG_RQST_GET_TABLE_ASYNC","MPEG_RQST_GET_TS_STREAM","MPEG_RQST_START_MPE_STREAM","MPEG_RQST_UNKNOWN","mpeg2structs/MPEG_REQUEST_TYPE","mpeg2structs/MPEG_RQST_GET_PES_STREAM","mpeg2structs/MPEG_RQST_GET_SECTION","mpeg2structs/MPEG_RQST_GET_SECTIONS_STREAM","mpeg2structs/MPEG_RQST_GET_SECTION_ASYNC","mpeg2structs/MPEG_RQST_GET_TABLE","mpeg2structs/MPEG_RQST_GET_TABLE_ASYNC","mpeg2structs/MPEG_RQST_GET_TS_STREAM","mpeg2structs/MPEG_RQST_START_MPE_STREAM","mpeg2structs/MPEG_RQST_UNKNOWN","mstv.mpeg_request_type"]
old-location: mstv\mpeg_request_type.htm
tech.root: mstv
ms.assetid: d1811cd5-3dda-48d1-a3b3-e4189e2622bb
ms.date: 12/05/2018
ms.keywords: MPEG_REQUEST_TYPE, MPEG_REQUEST_TYPE enumeration [Microsoft TV Technologies], MPEG_RQST_GET_PES_STREAM, MPEG_RQST_GET_SECTION, MPEG_RQST_GET_SECTIONS_STREAM, MPEG_RQST_GET_SECTION_ASYNC, MPEG_RQST_GET_TABLE, MPEG_RQST_GET_TABLE_ASYNC, MPEG_RQST_GET_TS_STREAM, MPEG_RQST_START_MPE_STREAM, MPEG_RQST_UNKNOWN, mpeg2structs/MPEG_REQUEST_TYPE, mpeg2structs/MPEG_RQST_GET_PES_STREAM, mpeg2structs/MPEG_RQST_GET_SECTION, mpeg2structs/MPEG_RQST_GET_SECTIONS_STREAM, mpeg2structs/MPEG_RQST_GET_SECTION_ASYNC, mpeg2structs/MPEG_RQST_GET_TABLE, mpeg2structs/MPEG_RQST_GET_TABLE_ASYNC, mpeg2structs/MPEG_RQST_GET_TS_STREAM, mpeg2structs/MPEG_RQST_START_MPE_STREAM, mpeg2structs/MPEG_RQST_UNKNOWN, mstv.mpeg_request_type
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
req.typenames: MPEG_REQUEST_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_mpeg2structs_0000_0000_0032
 - mpeg2structs/__MIDL___MIDL_itf_mpeg2structs_0000_0000_0032
 - MPEG_REQUEST_TYPE
 - mpeg2structs/MPEG_REQUEST_TYPE
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
 - MPEG_REQUEST_TYPE
---

# MPEG_REQUEST_TYPE enumeration


## -description

The <b>MPEG_REQUEST_TYPE</b> enumeration type specifies a request for MPEG-2 data.

## -enum-fields

### -field MPEG_RQST_UNKNOWN:0

Unknown request type. Do not use this value.

### -field MPEG_RQST_GET_SECTION

Get one table section. (Synchronous call.)

### -field MPEG_RQST_GET_SECTION_ASYNC

Get one table section. (Asynchronous call.)

### -field MPEG_RQST_GET_TABLE

Get a complete table. (Synchronous call.)

### -field MPEG_RQST_GET_TABLE_ASYNC

Get a complete table. (Asynchronous call.)

### -field MPEG_RQST_GET_SECTIONS_STREAM

Get a stream of sections.

### -field MPEG_RQST_GET_PES_STREAM

Get a stream of packetized elementary stream (PES) packets.

### -field MPEG_RQST_GET_TS_STREAM

Get a stream of transport stream (TS) packets.

### -field MPEG_RQST_START_MPE_STREAM

Get a stream of multi-protocol encapsulation (MPE) packets.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-types">BDA Enumeration Types</a>



<a href="/previous-versions/windows/desktop/api/mpeg2data/nf-mpeg2data-isectionlist-initialize">ISectionList::Initialize</a>
