---
UID: NS:mpeg2structs.__MIDL___MIDL_itf_mpeg2structs_0000_0000_0030
title: MPEG_CONTEXT (mpeg2structs.h)
description: The MPEG_CONTEXT structure identifies the source of an MPEG-2 data stream.
helpviewer_keywords: ["*PMPEG_CONTEXT","MPEG_CONTEXT","MPEG_CONTEXT structure [Microsoft TV Technologies]","mpeg2structs/MPEG_CONTEXT","mstv.mpeg_context"]
old-location: mstv\mpeg_context.htm
tech.root: mstv
ms.assetid: 7a92e545-805b-4ce6-bbf1-397f7a5f6524
ms.date: 12/05/2018
ms.keywords: '*PMPEG_CONTEXT, MPEG_CONTEXT, MPEG_CONTEXT structure [Microsoft TV Technologies], mpeg2structs/MPEG_CONTEXT, mstv.mpeg_context'
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
req.typenames: MPEG_CONTEXT, *PMPEG_CONTEXT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_mpeg2structs_0000_0000_0030
 - mpeg2structs/__MIDL___MIDL_itf_mpeg2structs_0000_0000_0030
 - PMPEG_CONTEXT
 - mpeg2structs/PMPEG_CONTEXT
 - MPEG_CONTEXT
 - mpeg2structs/MPEG_CONTEXT
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
 - MPEG_CONTEXT
---

# MPEG_CONTEXT structure


## -description

The <b>MPEG_CONTEXT</b> structure identifies the source of an MPEG-2 data stream.

## -struct-fields

### -field Type

Specifies the source type, as an <a href="/previous-versions/windows/desktop/api/mpeg2structs/ne-mpeg2structs-mpeg_context_type">MPEG_CONTEXT_TYPE</a> value. Currently, the value must be MPEG_CONTEXT_BCS_DEMUX.

### -field U

A union that contains the following members.

### -field U.Demux

Specifies an <a href="/previous-versions/windows/desktop/api/mpeg2structs/ns-mpeg2structs-mpeg_bcs_demux">MPEG_BCS_DEMUX</a> structure that identifies the filter graph instance.

### -field U.Winsock

Currently not supported.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-structures">BDA Structures</a>