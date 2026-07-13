---
UID: NS:mpeg2bits.MPEG_HEADER_VERSION_BITS
title: MPEG_HEADER_VERSION_BITS (mpeg2bits.h)
description: The MPEG_HEADER_VERSION_BITS structure contains the first 8 bits following the TSID in an MPEG-2 PSI section. These bits contain the version number and the current/next indicator.
helpviewer_keywords: ["*PMPEG_HEADER_VERSION_BITS","MPEG_HEADER_VERSION_BITS","MPEG_HEADER_VERSION_BITS structure [Microsoft TV Technologies]","MPEG_HEADER_VERSION_BITSStructure","PMPEG_HEADER_VERSION_BITS","PMPEG_HEADER_VERSION_BITS structure pointer [Microsoft TV Technologies]","mpeg2bits/MPEG_HEADER_VERSION_BITS","mpeg2bits/PMPEG_HEADER_VERSION_BITS","mstv.mpeg_header_version_bits"]
old-location: mstv\mpeg_header_version_bits.htm
tech.root: mstv
ms.assetid: d9a33ca6-2e35-4f7c-8621-ce30effeb687
ms.date: 12/05/2018
ms.keywords: '*PMPEG_HEADER_VERSION_BITS, MPEG_HEADER_VERSION_BITS, MPEG_HEADER_VERSION_BITS structure [Microsoft TV Technologies], MPEG_HEADER_VERSION_BITSStructure, PMPEG_HEADER_VERSION_BITS, PMPEG_HEADER_VERSION_BITS structure pointer [Microsoft TV Technologies], mpeg2bits/MPEG_HEADER_VERSION_BITS, mpeg2bits/PMPEG_HEADER_VERSION_BITS, mstv.mpeg_header_version_bits'
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
req.typenames: MPEG_HEADER_VERSION_BITS, *PMPEG_HEADER_VERSION_BITS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PMPEG_HEADER_VERSION_BITS
 - mpeg2bits/PMPEG_HEADER_VERSION_BITS
 - MPEG_HEADER_VERSION_BITS
 - mpeg2bits/MPEG_HEADER_VERSION_BITS
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
 - MPEG_HEADER_VERSION_BITS
---

# MPEG_HEADER_VERSION_BITS structure


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>MPEG_HEADER_VERSION_BITS</b> structure contains the first 8 bits following the TSID in an MPEG-2 PSI section. These bits contain the version number and the current/next indicator.

## -struct-fields

### -field CurrentNextIndicator

The current_next_indicator field.

### -field VersionNumber

The version_number field.

### -field Reserved

Two reserved bits.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-structures">BDA Structures</a>

