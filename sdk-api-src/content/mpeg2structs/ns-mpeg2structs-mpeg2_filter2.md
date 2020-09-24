---
UID: NS:mpeg2structs.__MIDL___MIDL_itf_mpeg2structs_0000_0000_0020
title: MPEG2_FILTER2 (mpeg2structs.h)
description: The MPEG2_FILTER2 structure specifies criteria for matching MPEG-2 section headers.
helpviewer_keywords: ["*PMPEG2_FILTER2","MPEG2_FILTER2","MPEG2_FILTER2 structure [Microsoft TV Technologies]","PMPEG2_FILTER2","PMPEG2_FILTER2 structure pointer [Microsoft TV Technologies]","mpeg2structs/MPEG2_FILTER","mpeg2structs/PMPEG2_FILTER2","mstv.mpeg2_filter2"]
old-location: mstv\mpeg2_filter2.htm
tech.root: mstv
ms.assetid: 3828f80f-23dc-4028-95d6-d85c007a44ec
ms.date: 12/05/2018
ms.keywords: '*PMPEG2_FILTER2, MPEG2_FILTER2, MPEG2_FILTER2 structure [Microsoft TV Technologies], PMPEG2_FILTER2, PMPEG2_FILTER2 structure pointer [Microsoft TV Technologies], mpeg2structs/MPEG2_FILTER, mpeg2structs/PMPEG2_FILTER2, mstv.mpeg2_filter2'
req.header: mpeg2structs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: MPEG2_FILTER2, *PMPEG2_FILTER2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_mpeg2structs_0000_0000_0020
 - mpeg2structs/__MIDL___MIDL_itf_mpeg2structs_0000_0000_0020
 - PMPEG2_FILTER2
 - mpeg2structs/PMPEG2_FILTER2
 - MPEG2_FILTER2
 - mpeg2structs/MPEG2_FILTER2
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
 - MPEG2_FILTER2
---

# MPEG2_FILTER2 structure


## -description

The <b>MPEG2_FILTER2</b> structure specifies criteria for matching MPEG-2 section headers.

## -struct-fields

### -field bVersionNumber

The version number of the structure. This value must be 2 or higher.

### -field wFilterSize

The size of the structure data, excluding any padding bytes. Set this field equal to the constant <b>MPEG2_FILTER_VERSION_2_SIZE</b>.

### -field fUseRawFilteringBits

If <b>TRUE</b>, the <b>Filter</b> and <b>Mask</b> members specify the filtering criteria as a pair of bit masks, and the remaining members of this structure are ignored. If <b>FALSE</b>, the <b>Filter</b> and <b>Mask</b> members are ignored, and the other structure members give the filtering criteria.

### -field Filter

A 16-byte bit mask, which contains the bit values to match in the section header.

### -field Mask

A 16-byte bit mask. For each bit, if the value in <b>Mask</b> is 0, the corresponding bit in <b>Filter</b> is matched against that bit in the section header. If the value in <b>Mask</b> is 1, that bit in the section header is ignored.

### -field fSpecifyTableIdExtension

If <b>TRUE</b>, the <b>table_ID_extension</b> field in the header must match the value of the <b>TableIdExtension</b> structure member. Otherwise, the <b>table_ID_extension field</b> is ignored.

### -field TableIdExtension

A value for the <b>table_ID_extension</b> field.

### -field fSpecifyVersion

If <b>TRUE</b>, the version_number field in the header must match the value of the <b>Version</b>  member. Otherwise, the <b>version_number</b> field is ignored.

### -field Version

A value for the <b>version_number</b> field.

### -field fSpecifySectionNumber

If <b>TRUE</b>, the <b>section_number</b> field in the header must match the value of the <b>SectionNumber</b>  member. Otherwise, the <b>section_number</b> field is ignored.

### -field SectionNumber

A value for the <b>section_number</b> field.

### -field fSpecifyCurrentNext

If <b>TRUE</b>, the <b>current_next_indicator</b> bit in the header must match the value of the <b>fNext</b> member. Otherwise, the <b>current_next_indicator</b> field is ignored.

### -field fNext

A value for the <b>current_next_indicator</b> bit. You can use the <a href="/previous-versions/windows/desktop/api/mpeg2structs/ne-mpeg2structs-mpeg_current_next_bit">MPEG_CURRENT_NEXT_BIT</a> enumeration type to specify this value.

### -field fSpecifyDsmccOptions

If <b>TRUE</b>, the <b>Dsmcc</b> member contains additional filtering criteria for the DSM-CC portions of the section header. Otherwise, the <b>Dsmcc</b> member is ignored.

### -field Dsmcc

A <a href="/previous-versions/windows/desktop/api/mpeg2structs/ns-mpeg2structs-dsmcc_filter_options">DSMCC_FILTER_OPTIONS</a> structure that contains additional filtering criteria for the DSM-CC portions of the section header.

### -field fSpecifyAtscOptions

If <b>TRUE</b>, the <b>Atsc</b> member contains additional filtering criteria. Otherwise, the <b>Atsc</b> member is ignored.

### -field Atsc

An <a href="/previous-versions/windows/desktop/api/mpeg2structs/ns-mpeg2structs-atsc_filter_options">ATSC_FILTER_OPTIONS</a> structure that contains additional filtering criteria.

### -field bVersion1Bytes

### -field fSpecifyDvbEitOptions

If <b>TRUE</b>, the <b>Dvb_Eit</b> member contains additional filtering criteria. Otherwise, the <b>Dvb_Eit</b> member is ignored. <div class="alert"><b>Note</b>  Requires Windows 7 or later.</div>
<div> </div>

### -field DvbEit

An <a href="/previous-versions/windows/desktop/api/mpeg2structs/ns-mpeg2structs-dvb_eit_filter_options">DVB_EIT_FILTER_OPTIONS</a> structure that contains additional filtering criteria. 



          

<div class="alert"><b>Note</b>  Requires Windows 7 or later.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-structures">BDA Structures</a>