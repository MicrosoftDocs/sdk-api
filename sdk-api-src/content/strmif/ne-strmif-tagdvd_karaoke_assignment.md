---
UID: NE:strmif.tagDVD_KARAOKE_ASSIGNMENT
title: tagDVD_KARAOKE_ASSIGNMENT
author: windows-sdk-content
description: Defines the speaker configuration for an audio stream.
old-location: dshow\dvd_karaoke_assignment.htm
old-project: DirectShow
ms.assetid: cdfd05b9-7a4a-49cc-ab50-bbe83ed9e0f0
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: DVD_Assignment_LR, DVD_Assignment_LR1, DVD_Assignment_LR12, DVD_Assignment_LRM, DVD_Assignment_LRM1, DVD_Assignment_LRM12, DVD_Assignment_reserved0, DVD_Assignment_reserved1, DVD_KARAOKE_ASSIGNMENT, DVD_KARAOKE_ASSIGNMENT , DVD_KARAOKE_ASSIGNMENT enumeration [DirectShow], DVD_KARAOKE_ASSIGNMENTEnumeration, dshow.dvd_karaoke_assignment, strmif/DVD_Assignment_LR, strmif/DVD_Assignment_LR1, strmif/DVD_Assignment_LR12, strmif/DVD_Assignment_LRM, strmif/DVD_Assignment_LRM1, strmif/DVD_Assignment_LRM12, strmif/DVD_Assignment_reserved0, strmif/DVD_Assignment_reserved1, strmif/DVD_KARAOKE_ASSIGNMENT, tagDVD_KARAOKE_ASSIGNMENT
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: strmif.h
req.include-header: Dshow.h
req.redist: 
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
tech.root: 
req.typenames: DVD_KARAOKE_ASSIGNMENT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - DVD_KARAOKE_ASSIGNMENT
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Outlook Express 6.0
---

# tagDVD_KARAOKE_ASSIGNMENT enumeration


## -description



Defines the speaker configuration for an audio stream.




## -enum-fields




### -field DVD_Assignment_reserved0

Reserved.
          


### -field DVD_Assignment_reserved1

Reserved.
          


### -field DVD_Assignment_LR

The stream is assigned to the left and right speakers.
          


### -field DVD_Assignment_LRM

The stream is assigned to the left, right, and middle speakers.
          


### -field DVD_Assignment_LR1

The stream is assigned to the left, right, and audio1 speakers.
          


### -field DVD_Assignment_LRM1

The stream is assigned to the left, right, middle, and audio1 speakers.
          


### -field DVD_Assignment_LR12

The stream is assigned to the left, right, and audio2 speakers.
          


### -field DVD_Assignment_LRM12

The stream is assigned to the left, right, middle, and audio2 speakers.
          


## -remarks



All channels within a stream will use the same speaker configuration, although the channels can be sent to different speakers within this configuration.




## -see-also




<a href="https://msdn.microsoft.com/dffb0b0e-edce-47e7-b9c0-983fdd2c4746">DVD_KaraokeAttributes Structure</a>



<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>
 

 

