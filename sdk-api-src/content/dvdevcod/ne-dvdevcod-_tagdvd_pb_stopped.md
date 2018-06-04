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

# _tagDVD_PB_STOPPED enumeration


## -description



The DVD_PB_STOPPED enumeration value has flags that indicate why DVD playback stopped. This flag is sent in the <i>lParam1</i> parameter of the <a href="https://msdn.microsoft.com/c8617307-d70e-48af-8e85-69105595aa10">EC_DVD_PLAYBACK_STOPPED</a> event.




## -enum-fields




### -field DVD_PB_STOPPED_Other


            Unspecified reason.
          


### -field DVD_PB_STOPPED_NoBranch


            The current program chain (PGC) completed and the DVD Navigator found no other video or other branching instructions.
          


### -field DVD_PB_STOPPED_NoFirstPlayDomain


            The disc does not contain an initial startup program.
          


### -field DVD_PB_STOPPED_StopCommand


            The application stopped playback or a DVD Navigator reached a stop command on the disc.
          


### -field DVD_PB_STOPPED_Reset


            The DVD Navigator was reset to the start of the disc.
          


### -field DVD_PB_STOPPED_DiscEjected


            The disc was ejected.
          


### -field DVD_PB_STOPPED_IllegalNavCommand


            An invalid navigation command prevented playback from continuing.
          


### -field DVD_PB_STOPPED_PlayPeriodAutoStop


            Playback reached the end time that was specified by the application.
          


### -field DVD_PB_STOPPED_PlayChapterAutoStop


            Playback reached the end of the chapter.
          


### -field DVD_PB_STOPPED_ParentalFailure


            Playback was stopped because of the parental level.
          


### -field DVD_PB_STOPPED_RegionFailure


            Playback was stopped because the region did not match.
          


### -field DVD_PB_STOPPED_MacrovisionFailure


            Playback was stopped because of analog copy protection.
          


### -field DVD_PB_STOPPED_DiscReadError


            An error occurred while reading the disc.
          


### -field DVD_PB_STOPPED_CopyProtectFailure


            Playback was stopped because of copy protection.
          


### -field DVD_PB_STOPPED_CopyProtectOutputFailure

The disc cannot be played because the video display does not meet the copy protection requirements. 
            


### -field DVD_PB_STOPPED_CopyProtectOutputNotSupported


            The disc cannot be played because the driver does not support checking the video display.


## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>
 

 

