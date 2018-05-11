---
UID: NE:strmif.tagDVD_KARAOKE_DOWNMIX
title: tagDVD_KARAOKE_DOWNMIX
author: windows-driver-content
description: Defines flags used by the IDvdControl2::SelectKaraokeAudioPresentationMode method to control which speakers, if any, each auxiliary channel is downmixed to.
old-location: dshow\dvd_karaoke_downmix.htm
old-project: DirectShow
ms.assetid: 7f0132ae-6a46-4b81-9c5b-a0399a429b1a
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: DVD_KARAOKE_DOWNMIX, DVD_KARAOKE_DOWNMIX , DVD_KARAOKE_DOWNMIX enumeration [DirectShow], DVD_KARAOKE_DOWNMIXEnumeration, DVD_Mix_0to0, DVD_Mix_0to1, DVD_Mix_1to0, DVD_Mix_1to1, DVD_Mix_2to0, DVD_Mix_2to1, DVD_Mix_3to0, DVD_Mix_3to1, DVD_Mix_4to0, DVD_Mix_4to1, DVD_Mix_Lto0, DVD_Mix_Lto1, DVD_Mix_Rto0, DVD_Mix_Rto1, dshow.dvd_karaoke_downmix, strmif/DVD_KARAOKE_DOWNMIX, strmif/DVD_Mix_0to0, strmif/DVD_Mix_0to1, strmif/DVD_Mix_1to0, strmif/DVD_Mix_1to1, strmif/DVD_Mix_2to0, strmif/DVD_Mix_2to1, strmif/DVD_Mix_3to0, strmif/DVD_Mix_3to1, strmif/DVD_Mix_4to0, strmif/DVD_Mix_4to1, strmif/DVD_Mix_Lto0, strmif/DVD_Mix_Lto1, strmif/DVD_Mix_Rto0, strmif/DVD_Mix_Rto1, tagDVD_KARAOKE_DOWNMIX
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: strmif.h
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
req.typenames: DVD_KARAOKE_DOWNMIX
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	strmif.h
api_name:
-	DVD_KARAOKE_DOWNMIX
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Internet Explorer 6.01
---

# tagDVD_KARAOKE_DOWNMIX enumeration


## -description



Defines flags used by the <a href="https://msdn.microsoft.com/9101fd83-1349-4cdd-b5e9-6daeb7d1e3d8">IDvdControl2::SelectKaraokeAudioPresentationMode</a> method to control which speakers, if any, each auxiliary channel is downmixed to.




## -enum-fields




### -field DVD_Mix_0to0


            Reserved.
          


### -field DVD_Mix_1to0


            Reserved.
          


### -field DVD_Mix_2to0

Downmix channel 2 to the left speaker.


### -field DVD_Mix_3to0

Downmix channel 3 to the left speaker.


### -field DVD_Mix_4to0

Downmix channel 4 to the left speaker.


### -field DVD_Mix_Lto0


            Reserved.
          


### -field DVD_Mix_Rto0


            Reserved.
          


### -field DVD_Mix_0to1


            Reserved.
          


### -field DVD_Mix_1to1


            Reserved.
          


### -field DVD_Mix_2to1

Downmix channel 2 to the right speaker.


### -field DVD_Mix_3to1

Downmix channel 3 to the right speaker.


### -field DVD_Mix_4to1

Downmix channel 4 to the right speaker.


### -field DVD_Mix_Lto1


            Reserved.
          


### -field DVD_Mix_Rto1


            Reserved.
          


## -remarks



Audio channels are zero-based, so channels 2 through 4 are the three auxiliary karaoke channels. Use bitwise <b>OR</b> operations to set the appropriate bit to send a channel to the left speaker (0), right speaker (1), both speakers, or to no speakers by turning both bits off. These bits are all off by default whenever the <a href="https://msdn.microsoft.com/3b2c01a2-d52c-4497-8fc9-d1113e8507e8">DVD Navigator Filter</a> filter enters karaoke mode.




## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/9101fd83-1349-4cdd-b5e9-6daeb7d1e3d8">IDvdControl2::SelectKaraokeAudioPresentationMode</a>
 

 

