---
UID: NS:mpeg2structs.__MIDL___MIDL_itf_mpeg2structs_0000_0000_0017
title: ATSC_FILTER_OPTIONS (mpeg2structs.h)
description: The ATSC_FILTER_OPTIONS structure specifies additional criteria for matching ATSC section headers.
helpviewer_keywords: ["ATSC_FILTER_OPTIONS","ATSC_FILTER_OPTIONS structure [Microsoft TV Technologies]","__MIDL___MIDL_itf_mpeg2structs_0000_0000_0017","mpeg2structs/ATSC_FILTER_OPTIONS","mstv.atsc_filter_options"]
old-location: mstv\atsc_filter_options.htm
tech.root: mstv
ms.assetid: 16e33f92-9e25-4a03-a21f-0ea5a99470ee
ms.date: 12/05/2018
ms.keywords: ATSC_FILTER_OPTIONS, ATSC_FILTER_OPTIONS structure [Microsoft TV Technologies], __MIDL___MIDL_itf_mpeg2structs_0000_0000_0017, mpeg2structs/ATSC_FILTER_OPTIONS, mstv.atsc_filter_options
req.header: mpeg2structs.h
req.include-header: Mpeg2data.h
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
req.typenames: ATSC_FILTER_OPTIONS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_mpeg2structs_0000_0000_0017
 - mpeg2structs/__MIDL___MIDL_itf_mpeg2structs_0000_0000_0017
 - ATSC_FILTER_OPTIONS
 - mpeg2structs/ATSC_FILTER_OPTIONS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mpeg2structs.h
api_name:
 - ATSC_FILTER_OPTIONS
---

# ATSC_FILTER_OPTIONS structure


## -description

The <b>ATSC_FILTER_OPTIONS</b> structure specifies additional criteria for matching ATSC section headers.

## -struct-fields

### -field fSpecifyEtmId

If this flag is <b>TRUE</b>, the ETM_id field in the header must match the value of the <b>EtmId</b> structure member. Otherwise, the ETM_id field is ignored.

### -field EtmId

Specifies a value for the ETM_id field.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-structures">BDA Structures</a>



<a href="/previous-versions/windows/desktop/api/mpeg2structs/ns-mpeg2structs-mpeg2_filter">MPEG2_FILTER Structure</a>