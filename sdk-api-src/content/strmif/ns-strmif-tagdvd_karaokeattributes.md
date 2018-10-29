---
UID: NS:strmif.tagDVD_KaraokeAttributes
title: tagDVD_KaraokeAttributes
author: windows-sdk-content
description: The DVD_KaraokeAttributes structure contains information about a karaoke audio stream. The IDvdInfo2::GetKaraokeAttributes method fills in a DVD_KaraokeAttributes structure for a specified stream.
old-location: dshow\dvd_karaokeattributes.htm
tech.root: DirectShow
ms.assetid: dffb0b0e-edce-47e7-b9c0-983fdd2c4746
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: DVD_KaraokeAttributes, DVD_KaraokeAttributes structure [DirectShow], DVD_KaraokeAttributesStructure, dshow.dvd_karaokeattributes, strmif/DVD_KaraokeAttributes, tagDVD_KaraokeAttributes
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
---

# tagDVD_KaraokeAttributes structure


## -description



The <code>DVD_KaraokeAttributes</code> structure contains information about a karaoke audio stream. The <a href="https://msdn.microsoft.com/c69ea1e0-8d8a-4cd3-86a4-a2d481160a2e">IDvdInfo2::GetKaraokeAttributes</a> method fills in a <code>DVD_KaraokeAttributes</code> structure for a specified stream.




## -struct-fields




### -field bVersion

Version number. The current karaoke version is 1.0.


### -field fMasterOfCeremoniesInGuideVocal1

If <b>TRUE</b>, the "Guide Vocal 1" channel contains the "Master of Ceremonies" content.


### -field fDuet

A Boolean value indicating whether the song is intended to be sung as a duet.


### -field ChannelAssignment

A <a href="https://msdn.microsoft.com/cdfd05b9-7a4a-49cc-ab50-bbe83ed9e0f0">DVD_KARAOKE_ASSIGNMENT</a> value indicating the speaker configuration into which all the channels will be mixed.


### -field wChannelContents

An array of valid <a href="https://msdn.microsoft.com/9d02b0bf-237a-42bf-b946-588b899cd3d9">DVD_KARAOKE_CONTENTS</a> values that identifies the content on each channel.


## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>
 

 

