---
UID: NS:amvideo.tagMPEG1VIDEOINFO
title: MPEG1VIDEOINFO (amvideo.h)

description: The MPEG1VIDEOINFO structure describes an MPEG-1 video stream.
old-location: dshow\mpeg1videoinfo.htm
tech.root: DirectShow
ms.assetid: ae5b8825-7c1c-4a44-b665-098732e6c3bc

ms.date: 12/05/2018
ms.keywords: MPEG1VIDEOINFO, MPEG1VIDEOINFO structure [DirectShow], MPEG1VIDEOINFOStructure, amvideo/MPEG1VIDEOINFO, dshow.mpeg1videoinfo, tagMPEG1VIDEOINFO
ms.topic: struct
f1_keywords: 
 - "amvideo/MPEG1VIDEOINFO"
dev_langs:
 - c++
req.header: amvideo.h
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
 - amvideo.h
api_name:
 - MPEG1VIDEOINFO
targetos: Windows
req.typenames: MPEG1VIDEOINFO
req.redist: 
ms.custom: 19H1
---

# MPEG1VIDEOINFO structure


## -description



The <b>MPEG1VIDEOINFO</b> structure describes an MPEG-1 video stream.




## -struct-fields




### -field hdr


<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader">VIDEOINFOHEADER</a> structure.


### -field dwStartTimeCode

25-bit group-of-pictures (GOP) time code at start of data.


### -field cbSequenceHeader

Length of the <b>bSequenceHeader</b> member, in bytes.


### -field bSequenceHeader

Start of an array that contains the sequence header, including quantization matrices, if any. The size of the array is given in the <b>cbSequenceHeader</b> member.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>
 

 

