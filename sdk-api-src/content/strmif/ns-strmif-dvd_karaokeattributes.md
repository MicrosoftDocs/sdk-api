---
UID: NS:strmif.tagDVD_KaraokeAttributes
title: DVD_KaraokeAttributes (strmif.h)
author: windows-sdk-content
description: The DVD_KaraokeAttributes structure contains information about a karaoke audio stream. The IDvdInfo2::GetKaraokeAttributes method fills in a DVD_KaraokeAttributes structure for a specified stream.
old-location: dshow\dvd_karaokeattributes.htm
tech.root: DirectShow
ms.assetid: dffb0b0e-edce-47e7-b9c0-983fdd2c4746
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DVD_KaraokeAttributes, DVD_KaraokeAttributes structure [DirectShow], DVD_KaraokeAttributesStructure, dshow.dvd_karaokeattributes, strmif/DVD_KaraokeAttributes
ms.topic: struct
f1_keywords: 
 - "strmif/DVD_KaraokeAttributes"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - DVD_KaraokeAttributes
product: Windows
targetos: Windows
req.typenames: DVD_KaraokeAttributes
req.redist: 
ms.custom: 19H1
---

# DVD_KaraokeAttributes structure


## -description



The <code>DVD_KaraokeAttributes</code> structure contains information about a karaoke audio stream. The <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getkaraokeattributes">IDvdInfo2::GetKaraokeAttributes</a> method fills in a <code>DVD_KaraokeAttributes</code> structure for a specified stream.




## -struct-fields




### -field bVersion

Version number. The current karaoke version is 1.0.


### -field fMasterOfCeremoniesInGuideVocal1

If <b>TRUE</b>, the "Guide Vocal 1" channel contains the "Master of Ceremonies" content.


### -field fDuet

A Boolean value indicating whether the song is intended to be sung as a duet.


### -field ChannelAssignment

A <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-tagdvd_karaoke_assignment">DVD_KARAOKE_ASSIGNMENT</a> value indicating the speaker configuration into which all the channels will be mixed.


### -field wChannelContents

An array of valid <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-tagdvd_karaoke_contents">DVD_KARAOKE_CONTENTS</a> values that identifies the content on each channel.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>
 

 

