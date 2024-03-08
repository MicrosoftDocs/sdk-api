---
UID: NS:mpeg2bits.MPEG_HEADER_BITS
title: MPEG_HEADER_BITS (mpeg2bits.h)
description: The MPEG_HEADER_BITS structure contains the first 16 bits that follow the table_id in a generic MPEG-2 section header.
helpviewer_keywords: ["*PMPEG_HEADER_BITS","MPEG_HEADER_BITS","MPEG_HEADER_BITS structure [Microsoft TV Technologies]","MPEG_HEADER_BITSStructure","PMPEG_HEADER_BITS","PMPEG_HEADER_BITS structure pointer [Microsoft TV Technologies]","mpeg2bits/MPEG_HEADER_BITS","mpeg2bits/PMPEG_HEADER_BITS","mstv.mpeg_header_bits"]
old-location: mstv\mpeg_header_bits.htm
tech.root: mstv
ms.assetid: e25d36af-ee72-4986-8d96-2bce8b19ac80
ms.date: 12/05/2018
ms.keywords: '*PMPEG_HEADER_BITS, MPEG_HEADER_BITS, MPEG_HEADER_BITS structure [Microsoft TV Technologies], MPEG_HEADER_BITSStructure, PMPEG_HEADER_BITS, PMPEG_HEADER_BITS structure pointer [Microsoft TV Technologies], mpeg2bits/MPEG_HEADER_BITS, mpeg2bits/PMPEG_HEADER_BITS, mstv.mpeg_header_bits'
req.header: mpeg2bits.h
req.include-header: Mpeg2Structs.h
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
req.typenames: MPEG_HEADER_BITS, *PMPEG_HEADER_BITS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PMPEG_HEADER_BITS
 - mpeg2bits/PMPEG_HEADER_BITS
 - MPEG_HEADER_BITS
 - mpeg2bits/MPEG_HEADER_BITS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mpeg2Bits.h
api_name:
 - MPEG_HEADER_BITS
---

# MPEG_HEADER_BITS structure


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>MPEG_HEADER_BITS</b> structure contains the first 16 bits that follow the table_id in a generic MPEG-2 section header.

## -struct-fields

### -field SectionLength

The length of the section, in bytes.

### -field Reserved

Two reserved bits.

### -field PrivateIndicator

The private_indicator bit.

### -field SectionSyntaxIndicator

The section_syntax_indicator bit.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-structures">BDA Structures</a>



<a href="/previous-versions/windows/desktop/api/mpeg2structs/ns-mpeg2structs-section">SECTION Structure</a>

