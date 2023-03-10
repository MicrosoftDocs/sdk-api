---
UID: NS:mpeg2structs.__MIDL___MIDL_itf_mpeg2structs_0000_0000_0018
title: DVB_EIT_FILTER_OPTIONS (mpeg2structs.h)
description: Specifies a section within a Digital Video Broadcast (DVB) Event Information Table (EIT) section header. Because the EIT can be quite large, these options allow applications to reduce load time by filtering specific segments from the EIT section header.
helpviewer_keywords: ["DVB_EIT_FILTER_OPTIONS","DVB_EIT_FILTER_OPTIONS structure [Microsoft TV Technologies]","PDVB_EIT_FILTER_OPTIONS","PDVB_EIT_FILTER_OPTIONS structure pointer [Microsoft TV Technologies]","mpeg2structs/DVB_EIT_FILTER_OPTIONS","mpeg2structs/PDVB_EIT_FILTER_OPTIONS","mstv.dvb_eit_filter_options"]
old-location: mstv\dvb_eit_filter_options.htm
tech.root: mstv
ms.assetid: 7bdbb67b-ff20-4f2a-ad8a-8bb8dba3da65
ms.date: 12/05/2018
ms.keywords: DVB_EIT_FILTER_OPTIONS, DVB_EIT_FILTER_OPTIONS structure [Microsoft TV Technologies], PDVB_EIT_FILTER_OPTIONS, PDVB_EIT_FILTER_OPTIONS structure pointer [Microsoft TV Technologies], mpeg2structs/DVB_EIT_FILTER_OPTIONS, mpeg2structs/PDVB_EIT_FILTER_OPTIONS, mstv.dvb_eit_filter_options
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
req.typenames: DVB_EIT_FILTER_OPTIONS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_mpeg2structs_0000_0000_0018
 - mpeg2structs/__MIDL___MIDL_itf_mpeg2structs_0000_0000_0018
 - DVB_EIT_FILTER_OPTIONS
 - mpeg2structs/DVB_EIT_FILTER_OPTIONS
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
 - DVB_EIT_FILTER_OPTIONS
---

# DVB_EIT_FILTER_OPTIONS structure


## -description

Specifies a section within a Digital Video Broadcast (DVB) Event Information Table (EIT) section header. Because the EIT can be quite large, these options allow applications to reduce load time by filtering specific segments from the EIT section header.

## -struct-fields

### -field fSpecifySegment

If this flag is <b>TRUE</b>, the number of the segment that is queried from the header must match the value of the <b>bSegment</b> structure member. Otherwise, the segment field is ignored.

### -field bSegment

Specifies the segment within the EIT section header that is queried.

