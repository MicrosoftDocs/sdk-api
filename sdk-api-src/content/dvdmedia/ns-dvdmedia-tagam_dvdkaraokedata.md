---
UID: NS:dvdmedia.tagAM_DvdKaraokeData
title: tagAM_DvdKaraokeData
author: windows-driver-content
description: Specifies how to mix the karaoke audio channels.
old-location: dshow\am_dvdkaraokedata.htm
old-project: DirectShow
ms.assetid: 9fef2dd9-0a56-4e51-a64b-7f12c8f9a966
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: AM_DvdKaraokeData, AM_DvdKaraokeData structure [DirectShow], dshow.am_dvdkaraokedata, dvdmedia/AM_DvdKaraokeData, tagAM_DvdKaraokeData
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: dvdmedia.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Dvbsiparser.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: AM_DvdKaraokeData
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Dvdmedia.h
api_name:
-	AM_DvdKaraokeData
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# tagAM_DvdKaraokeData structure


## -description



Specifies how to mix the karaoke audio channels.




## -struct-fields




### -field dwDownmix

A bitwise OR of <a href="https://msdn.microsoft.com/7f0132ae-6a46-4b81-9c5b-a0399a429b1a">DVD_KARAOKE_DOWNMIX</a> flags telling the decoder which channels are downmixed to channels 0 or 1.


### -field dwSpeakerAssignment

A valid <a href="https://msdn.microsoft.com/cdfd05b9-7a4a-49cc-ab50-bbe83ed9e0f0">DVD_KARAOKE_ASSIGNMENT</a> value that indicates which speakers the output is going to.


## -remarks



This structure is used for the AM_PROPERTY_DVDKARAOKE_DATA property.




## -see-also




<a href="https://msdn.microsoft.com/78b2998b-d8b3-424d-85bc-872e64eb4a4f">DVD Karaoke Property Set</a>



<a href="https://msdn.microsoft.com/9101fd83-1349-4cdd-b5e9-6daeb7d1e3d8">SelectKaraokeAudioPresentationMode</a>
 

 

