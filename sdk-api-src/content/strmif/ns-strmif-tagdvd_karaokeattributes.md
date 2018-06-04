---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

