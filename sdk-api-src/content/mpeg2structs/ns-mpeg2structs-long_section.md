---
UID: NS:mpeg2structs.__MIDL___MIDL_itf_mpeg2structs_0000_0000_0008
title: LONG_SECTION (mpeg2structs.h)
description: The LONG_SECTION structure represents a long MPEG-2 section header. If a section contains a long header, you can cast a SECTION pointer to a LONG_SECTION pointer. For more information, see the Remarks section in the SECTION reference.
helpviewer_keywords: ["*PLONG_SECTION","LONG_SECTION","LONG_SECTION structure [Microsoft TV Technologies]","PLONG_SECTION","PLONG_SECTION structure pointer [Microsoft TV Technologies]","mpeg2structs/LONG_SECTION","mpeg2structs/PLONG_SECTION","mstv.long_section"]
old-location: mstv\long_section.htm
tech.root: mstv
ms.assetid: 1403971f-5165-484c-9aa3-0cd489985545
ms.date: 12/05/2018
ms.keywords: '*PLONG_SECTION, LONG_SECTION, LONG_SECTION structure [Microsoft TV Technologies], PLONG_SECTION, PLONG_SECTION structure pointer [Microsoft TV Technologies], mpeg2structs/LONG_SECTION, mpeg2structs/PLONG_SECTION, mstv.long_section'
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
req.typenames: LONG_SECTION, *PLONG_SECTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_mpeg2structs_0000_0000_0008
 - mpeg2structs/__MIDL___MIDL_itf_mpeg2structs_0000_0000_0008
 - PLONG_SECTION
 - mpeg2structs/PLONG_SECTION
 - LONG_SECTION
 - mpeg2structs/LONG_SECTION
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
 - LONG_SECTION
---

# LONG_SECTION structure


## -description

The <b>LONG_SECTION</b> structure represents a long MPEG-2 section header. If a section contains a long header, you can cast a <a href="/previous-versions/windows/desktop/api/mpeg2structs/ns-mpeg2structs-section">SECTION</a> pointer to a <b>LONG_SECTION</b> pointer. For more information, see the Remarks section in the <b>SECTION</b> reference.

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

### -field RemainingData

Contains the remaining section data, as a byte array. The length of the array is <code>Header.W.SectionLength - 5</code> bytes.

## -remarks

The following code shows how to access the bit fields within the <b>Version</b> member:


```cpp

LONG_SECTION *pSection; // Points to the section data.

// Coerce the Version field to an MPEG_HEADER_VERSION_BITS type.
MPEG_HEADER_VERSION_BITS *pVersion;
pVersion = (MPEG_HEADER_VERSION_BITS*)&pSection->Version.B;

// Now use the pHeader pointer to access the bit fields.
BYTE VersionNumber = pSection->VersionNumber;

```

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-structures">BDA Structures</a>