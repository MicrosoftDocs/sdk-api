---
UID: NS:mpeg2structs.__MIDL___MIDL_itf_mpeg2structs_0000_0000_0011
title: DSMCC_SECTION (mpeg2structs.h)
description: The DSMCC_SECTION structure represents a DSM-CC section header. If a section contains a DSM-CC header, you can cast a SECTION pointer to a DSMCC_SECTION pointer. For more information, see the Remarks section in the SECTION reference.
helpviewer_keywords: ["*PDSMCC_SECTION","DSMCC_SECTION","DSMCC_SECTION structure [Microsoft TV Technologies]","PDSMCC_SECTION","PDSMCC_SECTION structure pointer [Microsoft TV Technologies]","mpeg2structs/DSMCC_SECTION","mpeg2structs/PDSMCC_SECTION","mstv.dsmcc_section"]
old-location: mstv\dsmcc_section.htm
tech.root: mstv
ms.assetid: b043f63c-cee0-4167-9b11-09b747f63b8d
ms.date: 12/05/2018
ms.keywords: '*PDSMCC_SECTION, DSMCC_SECTION, DSMCC_SECTION structure [Microsoft TV Technologies], PDSMCC_SECTION, PDSMCC_SECTION structure pointer [Microsoft TV Technologies], mpeg2structs/DSMCC_SECTION, mpeg2structs/PDSMCC_SECTION, mstv.dsmcc_section'
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
req.typenames: DSMCC_SECTION, *PDSMCC_SECTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_mpeg2structs_0000_0000_0011
 - mpeg2structs/__MIDL___MIDL_itf_mpeg2structs_0000_0000_0011
 - PDSMCC_SECTION
 - mpeg2structs/PDSMCC_SECTION
 - DSMCC_SECTION
 - mpeg2structs/DSMCC_SECTION
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
 - DSMCC_SECTION
---

# DSMCC_SECTION structure


## -description

The <b>DSMCC_SECTION</b> structure represents a DSM-CC section header. If a section contains a DSM-CC header, you can cast a <a href="/previous-versions/windows/desktop/api/mpeg2structs/ns-mpeg2structs-section">SECTION</a> pointer to a <b>DSMCC_SECTION</b> pointer. For more information, see the Remarks section in the <b>SECTION</b> reference.

## -struct-fields

### -field TableId

Specifies the table identifier (TID) of the section.

### -field Header

A union that contains the following members.

### -field Header.S

Contains packed header bits, as an <b>MPEG_HEADER_BITS_MIDL</b> structure. Applications should use the <b>Header.W</b> field instead.

### -field Header.W

Contains the header bits as a <b>WORD</b> type. To get the individual bitfields, coerce this member to an <a href="/previous-versions/windows/desktop/api/mpeg2bits/ns-mpeg2bits-mpeg_header_bits">MPEG_HEADER_BITS</a> structure.

### -field TableIdExtension

Specifies the table_id_extension field.

### -field Version

A union that contains the following members.

### -field Version.S

Contains the version number and current/next indicator bit as an <b>MPEG_HEADER_VERSION_BITS_MIDL</b> structure. Applications should use the <b>Version.B</b> field instead.

### -field Version.B

Contains the version number and current/next indicator bit as a <b>BYTE</b> type. To get the individual bit fields, coerce this member to an <a href="/previous-versions/windows/desktop/api/mpeg2bits/ns-mpeg2bits-mpeg_header_version_bits">MPEG_HEADER_VERSION_BITS</a> structure.

### -field SectionNumber

Specifies the section_number field, which gives the section number for this section.

### -field LastSectionNumber

Specifies the last_section_number field, which gives the last (highest) section number for the table.

### -field ProtocolDiscriminator

Indicates that the message is an MPEG-2 DSM-CC message. The value of this field is always 0x11.

### -field DsmccType

Specifies the DSM-CC message type.

### -field MessageId

Specifies the DSM-CC message identifier.

### -field TransactionId

Specifies the transaction identifier.

### -field Reserved

Reserved bytes.

### -field AdaptationLength

Specifies the adaptation field length.

### -field MessageLength

Specifies the message length.

### -field RemainingData

Contains the remaining section data, as a byte array. The length of the array is <code>Header.W.SectionLength - 17</code> bytes.

## -remarks

This structure extends the <a href="/previous-versions/windows/desktop/api/mpeg2structs/ns-mpeg2structs-long_section">LONG_SECTION</a> structure.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-structures">BDA Structures</a>