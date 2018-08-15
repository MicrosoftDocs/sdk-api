---
UID: NE:dvdevcod._tagDVD_PB_STOPPED
title: "_tagDVD_PB_STOPPED"
author: windows-sdk-content
description: The DVD_PB_STOPPED enumeration value has flags that indicate why DVD playback stopped. This flag is sent in the lParam1 parameter of the EC_DVD_PLAYBACK_STOPPED event.
old-location: dshow\dvd_pb_stopped.htm
old-project: DirectShow
ms.assetid: 7f095629-9d44-4666-b14a-932122959f4e
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: DVD_PB_STOPPED, DVD_PB_STOPPED , DVD_PB_STOPPED enumeration [DirectShow], DVD_PB_STOPPEDEnumeration, DVD_PB_STOPPED_CopyProtectFailure, DVD_PB_STOPPED_CopyProtectOutputFailure, DVD_PB_STOPPED_CopyProtectOutputNotSupported, DVD_PB_STOPPED_DiscEjected, DVD_PB_STOPPED_DiscReadError, DVD_PB_STOPPED_IllegalNavCommand, DVD_PB_STOPPED_MacrovisionFailure, DVD_PB_STOPPED_NoBranch, DVD_PB_STOPPED_NoFirstPlayDomain, DVD_PB_STOPPED_Other, DVD_PB_STOPPED_ParentalFailure, DVD_PB_STOPPED_PlayChapterAutoStop, DVD_PB_STOPPED_PlayPeriodAutoStop, DVD_PB_STOPPED_RegionFailure, DVD_PB_STOPPED_Reset, DVD_PB_STOPPED_StopCommand, _tagDVD_PB_STOPPED, dshow.dvd_pb_stopped, dvdevcod/DVD_PB_STOPPED, dvdevcod/DVD_PB_STOPPED_CopyProtectFailure, dvdevcod/DVD_PB_STOPPED_CopyProtectOutputFailure, dvdevcod/DVD_PB_STOPPED_CopyProtectOutputNotSupported, dvdevcod/DVD_PB_STOPPED_DiscEjected, dvdevcod/DVD_PB_STOPPED_DiscReadError, dvdevcod/DVD_PB_STOPPED_IllegalNavCommand, dvdevcod/DVD_PB_STOPPED_MacrovisionFailure, dvdevcod/DVD_PB_STOPPED_NoBranch, dvdevcod/DVD_PB_STOPPED_NoFirstPlayDomain, dvdevcod/DVD_PB_STOPPED_Other, dvdevcod/DVD_PB_STOPPED_ParentalFailure, dvdevcod/DVD_PB_STOPPED_PlayChapterAutoStop, dvdevcod/DVD_PB_STOPPED_PlayPeriodAutoStop, dvdevcod/DVD_PB_STOPPED_RegionFailure, dvdevcod/DVD_PB_STOPPED_Reset, dvdevcod/DVD_PB_STOPPED_StopCommand
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: dvdevcod.h
req.include-header: Dshow.h
req.redist: 
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
tech.root: 
req.typenames: DVD_PB_STOPPED
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dvdevcod.h
api_name:
 - DVD_PB_STOPPED
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
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
 

 

