---
UID: NS:mpeg2structs.__MIDL___MIDL_itf_mpeg2structs_0000_0000_0006
title: SECTION (mpeg2structs.h)
description: The SECTION structure represents a short header from an MPEG-2 table section.
helpviewer_keywords: ["*PSECTION","PSECTION","PSECTION structure pointer [Microsoft TV Technologies]","SECTION","SECTION structure [Microsoft TV Technologies]","mpeg2structs/PSECTION","mpeg2structs/SECTION","mstv.section"]
old-location: mstv\section.htm
tech.root: mstv
ms.assetid: 6ee07b84-ae97-413f-a3b4-0078ad740194
ms.date: 12/05/2018
ms.keywords: '*PSECTION, PSECTION, PSECTION structure pointer [Microsoft TV Technologies], SECTION, SECTION structure [Microsoft TV Technologies], mpeg2structs/PSECTION, mpeg2structs/SECTION, mstv.section'
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
req.typenames: SECTION, *PSECTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_mpeg2structs_0000_0000_0006
 - mpeg2structs/__MIDL___MIDL_itf_mpeg2structs_0000_0000_0006
 - PSECTION
 - mpeg2structs/PSECTION
 - SECTION
 - mpeg2structs/SECTION
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
 - SECTION
---

# SECTION structure


## -description

The <b>SECTION</b> structure represents a short header from an MPEG-2 table section.

## -struct-fields

### -field TableId

Specifies the table identifier (TID) of the section.

### -field Header

A union that contains the following members.

### -field Header.S

Contains header bits, as an <b>MPEG_HEADER_BITS_MIDL</b> structure. Applications should use the <b>Header.W</b> field instead.

### -field Header.W

Contains the header bits as a <b>WORD</b> type. To get the individual bit fields, coerce this member to an <a href="/previous-versions/windows/desktop/api/mpeg2bits/ns-mpeg2bits-mpeg_header_bits">MPEG_HEADER_BITS</a> structure.

### -field SectionData

Contains the section data, as a byte array. The length of the array is given by the <b>Header.W.SectionLength</b> field.

## -remarks

This structure represents an MPEG-2 short header. The section might contain a long header or DSM-CC header, each of which extends the short header:

<ul>
<li>If the <b>Header.W.SectionSyntaxIndicator</b> bit is set, the section uses the long syntax. In that case, you can cast a <b>SECTION</b> pointer to a <a href="/previous-versions/windows/desktop/api/mpeg2structs/ns-mpeg2structs-long_section">LONG_SECTION</a> pointer.</li>
<li>If the TID indicates a DSM-CC user-to-network message (0x3B) or a download data message (0x3C), the section uses the DSM-CC header syntax. In that case, you can cast a <b>SECTION</b> pointer to a <a href="/previous-versions/windows/desktop/api/mpeg2structs/ns-mpeg2structs-dsmcc_section">DSMCC_SECTION</a> pointer.</li>
</ul>
The following code shows how to access the bit fields within the <b>Header</b> member:


```cpp

SECTION *pSection; // Points to the section data.

// Coerce the Header field to an MPEG_HEADER_BITS type.
MPEG_HEADER_BITS *pHeader = (MPEG_HEADER_BITS*)&pSection->Header.W;

// Now use the pHeader pointer to access the bit fields.
WORD SectionLength = pHeader->SectionLength;

```

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-structures">BDA Structures</a>