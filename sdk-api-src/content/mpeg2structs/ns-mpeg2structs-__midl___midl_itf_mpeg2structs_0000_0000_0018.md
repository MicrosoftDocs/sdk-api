---
UID: NS:mpeg2structs.__MIDL___MIDL_itf_mpeg2structs_0000_0000_0018
title: "__MIDL___MIDL_itf_mpeg2structs_0000_0000_0018"
author: windows-sdk-content
description: Specifies a section within a Digital Video Broadcast (DVB) Event Information Table (EIT) section header. Because the EIT can be quite large, these options allow applications to reduce load time by filtering specific segments from the EIT section header.
old-location: mstv\dvb_eit_filter_options.htm
old-project: mstv
ms.assetid: 7bdbb67b-ff20-4f2a-ad8a-8bb8dba3da65
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: DVB_EIT_FILTER_OPTIONS, DVB_EIT_FILTER_OPTIONS structure [Microsoft TV Technologies], PDVB_EIT_FILTER_OPTIONS, PDVB_EIT_FILTER_OPTIONS structure pointer [Microsoft TV Technologies], __MIDL___MIDL_itf_mpeg2structs_0000_0000_0018, mpeg2structs/DVB_EIT_FILTER_OPTIONS, mpeg2structs/PDVB_EIT_FILTER_OPTIONS, mstv.dvb_eit_filter_options
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: DVB_EIT_FILTER_OPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mpeg2Structs.h
api_name:
 - DVB_EIT_FILTER_OPTIONS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# __MIDL___MIDL_itf_mpeg2structs_0000_0000_0018 structure


## -description


Specifies a section within a Digital Video Broadcast (DVB) Event Information Table (EIT) section header. Because the EIT can be quite large, these options allow applications to reduce load time by filtering specific segments from the EIT section header.


## -struct-fields




### -field fSpecifySegment

If this flag is <b>TRUE</b>, the number of the segment that is queried from the header must match the value of the <b>bSegment</b> structure member. Otherwise, the segment field is ignored.


### -field bSegment

Specifies the segment within the EIT section header that is queried.

