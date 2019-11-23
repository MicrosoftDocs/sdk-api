---
UID: NS:dvdmedia.tagAM_DvdKaraokeData
title: AM_DvdKaraokeData (dvdmedia.h)

description: Specifies how to mix the karaoke audio channels.
old-location: dshow\am_dvdkaraokedata.htm
tech.root: DirectShow
ms.assetid: 9fef2dd9-0a56-4e51-a64b-7f12c8f9a966

ms.date: 12/05/2018
ms.keywords: AM_DvdKaraokeData, AM_DvdKaraokeData structure [DirectShow], dshow.am_dvdkaraokedata, dvdmedia/AM_DvdKaraokeData
ms.topic: struct
f1_keywords: 
 - "dvdmedia/AM_DvdKaraokeData"
dev_langs:
 - c++
req.header: dvdmedia.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dvdmedia.h
api_name:
 - AM_DvdKaraokeData
targetos: Windows
req.typenames: AM_DvdKaraokeData
req.redist: 
ms.custom: 19H1
---

# AM_DvdKaraokeData structure


## -description



Specifies how to mix the karaoke audio channels.




## -struct-fields




### -field dwDownmix

A bitwise OR of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ne-strmif-dvd_karaoke_downmix">DVD_KARAOKE_DOWNMIX</a> flags telling the decoder which channels are downmixed to channels 0 or 1.


### -field dwSpeakerAssignment

A valid <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ne-strmif-dvd_karaoke_assignment">DVD_KARAOKE_ASSIGNMENT</a> value that indicates which speakers the output is going to.


## -remarks



This structure is used for the AM_PROPERTY_DVDKARAOKE_DATA property.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-karaoke-property-set">DVD Karaoke Property Set</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-selectkaraokeaudiopresentationmode">SelectKaraokeAudioPresentationMode</a>
 

 

