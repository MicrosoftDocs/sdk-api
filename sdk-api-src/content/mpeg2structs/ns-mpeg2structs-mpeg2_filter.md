---
UID: NS:mpeg2structs.__MIDL___MIDL_itf_mpeg2structs_0000_0000_0019
title: MPEG2_FILTER (mpeg2structs.h)
description: The MPEG2_FILTER structure specifies criteria for matching MPEG-2 section headers.
helpviewer_keywords: ["*PMPEG2_FILTER","MPEG2_FILTER","MPEG2_FILTER structure [Microsoft TV Technologies]","PMPEG2_FILTER","PMPEG2_FILTER structure pointer [Microsoft TV Technologies]","mpeg2structs/MPEG2_FILTER","mpeg2structs/PMPEG2_FILTER","mstv.mpeg2_filter"]
old-location: mstv\mpeg2_filter.htm
tech.root: mstv
ms.assetid: a7e66de7-d67b-4814-9849-076c3dd5afb1
ms.date: 12/05/2018
ms.keywords: '*PMPEG2_FILTER, MPEG2_FILTER, MPEG2_FILTER structure [Microsoft TV Technologies], PMPEG2_FILTER, PMPEG2_FILTER structure pointer [Microsoft TV Technologies], mpeg2structs/MPEG2_FILTER, mpeg2structs/PMPEG2_FILTER, mstv.mpeg2_filter'
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
req.typenames: MPEG2_FILTER, *PMPEG2_FILTER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_mpeg2structs_0000_0000_0019
 - mpeg2structs/__MIDL___MIDL_itf_mpeg2structs_0000_0000_0019
 - PMPEG2_FILTER
 - mpeg2structs/PMPEG2_FILTER
 - MPEG2_FILTER
 - mpeg2structs/MPEG2_FILTER
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
 - MPEG2_FILTER
---

# MPEG2_FILTER structure


## -description

The <b>MPEG2_FILTER</b> structure specifies criteria for matching MPEG-2 section headers.

## -struct-fields

### -field bVersionNumber

Specifies the version number of the structure. This value must be 1 or higher.

### -field wFilterSize

Specifies the size of the structure data, excluding any padding bytes. Set this field equal to the constant <b>MPEG2_FILTER_VERSION_1_SIZE</b>.

### -field fUseRawFilteringBits

If <b>TRUE</b>, the <b>Filter</b> and <b>Mask</b> members specify the filtering criteria as a pair of bit masks, and the remaining members of this structure are ignored. If this field is <b>FALSE</b>, the <b>Filter</b> and <b>Mask</b> members are ignored, and the other structure members contain the filtering criteria.

### -field Filter

Specifies a 16-byte bit mask, which contains the bit values to match in the section header.

### -field Mask

Specifies a 16-byte bit mask. Set any "don't care" bits equal to 1, and all other bits to 0. In other words, for each bit, if the value in <b>Mask</b> is 0, the corresponding bit in <b>Filter</b> will be matched against that bit in the section header. If the value in <b>Mask</b> is 1, that bit in the section header is ignored.

### -field fSpecifyTableIdExtension

If <b>TRUE</b>, the <b>table_ID_extension</b> field in the header must match the value of the <b>TableIdExtension</b> structure member. Otherwise, the <b>table_ID_extension</b> field is ignored.

### -field TableIdExtension

Specifies a value for the <b>table_ID_extension</b> field.

### -field fSpecifyVersion

If <b>TRUE</b>, the <b>version_number</b> field in the header must match the value of the <b>Version</b> structure member. Otherwise, the <b>version_number</b> field is ignored.

### -field Version

Specifies a value for the <b>version_number</b> field.

### -field fSpecifySectionNumber

If <b>TRUE</b>, the <b>section_number</b> field in the header must match the value of the <b>SectionNumber</b> member. Otherwise, the <b>section_number</b> field is ignored.

### -field SectionNumber

Specifies a value for the <b>section_number</b> field.

### -field fSpecifyCurrentNext

If <b>TRUE</b>, the <b>current_next_indicator</b> bit in the header must match the value of the <b>fNext</b> structure member. Otherwise, the <b>current_next_indicator</b> field is ignored.

### -field fNext

Specifies a value for the <b>current_next_indicator</b> bit. You can use the <a href="/previous-versions/windows/desktop/api/mpeg2structs/ne-mpeg2structs-mpeg_current_next_bit">MPEG_CURRENT_NEXT_BIT</a> enumeration type to specify this value.

### -field fSpecifyDsmccOptions

If <b>TRUE</b>, the <b>Dsmcc</b> member contains additional filtering criteria for the DSM-CC portions of the section header. Otherwise, the <b>Dsmcc</b> member is ignored.

### -field Dsmcc

Specifies a <a href="/previous-versions/windows/desktop/api/mpeg2structs/ns-mpeg2structs-dsmcc_filter_options">DSMCC_FILTER_OPTIONS</a> structure that contains additional filtering criteria for the DSM-CC portions of the section header.

### -field fSpecifyAtscOptions

If <b>TRUE</b>, the <b>Atsc</b> member contains additional filtering criteria. Otherwise, the <b>Atsc</b> member is ignored.

### -field Atsc

Specifies an <a href="/previous-versions/windows/desktop/api/mpeg2structs/ns-mpeg2structs-atsc_filter_options">ATSC_FILTER_OPTIONS</a> structure that contains additional filtering criteria.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-structures">BDA Structures</a>