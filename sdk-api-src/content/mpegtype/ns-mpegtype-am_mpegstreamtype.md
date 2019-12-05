---
UID: NS:mpegtype.tagAM_MPEGSTREAMTYPE
title: AM_MPEGSTREAMTYPE (mpegtype.h)
description: The AM_MPEGSTREAMTYPE structure defines the media type for an MPEG-1 program stream.
old-location: dshow\am_mpegstreamtype.htm
tech.root: DirectShow
ms.assetid: 8622ffcb-be64-4a8f-8bc7-834b559b0f95
ms.date: 12/05/2018
ms.keywords: AM_MPEGSTREAMTYPE, AM_MPEGSTREAMTYPE structure [DirectShow], dshow.am_mpegstreamtype, mpegtype/AM_MPEGSTREAMTYPE
ms.topic: struct
f1_keywords:
- mpegtype/AM_MPEGSTREAMTYPE
dev_langs:
- c++
req.header: mpegtype.h
req.include-header: Dshow.h
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- mpegtype.h
api_name:
- AM_MPEGSTREAMTYPE
targetos: Windows
req.typenames: AM_MPEGSTREAMTYPE
req.redist: 
ms.custom: 19H1
---

# AM_MPEGSTREAMTYPE structure


## -description


The <b>AM_MPEGSTREAMTYPE</b> structure defines the media type for an MPEG-1 program stream.
        


## -struct-fields




### -field dwStreamId

 


### -field dwReserved

Reserved.


### -field mt


<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ns-strmif-am_media_type">AM_MEDIA_TYPE</a> structure describing the type for the substeam. The <b>pbFormat</b> member of this structure must <b>NULL</b>. The format data normally conveyed in <b>pbFormat</b> is stored in the <b>bFormat</b> member.


### -field bFormat

Format data. The size of this array, in bytes, is given in the <b>mt.cbFormat</b> member.


#### - dwStreamID

Stream identifier of the stream to process.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mpegtype/ns-mpegtype-am_mpegsystemtype">AM_MPEGSYSTEMTYPE</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/mpeg-1-media-types">MEPG-1 Media Types</a>
 

 

