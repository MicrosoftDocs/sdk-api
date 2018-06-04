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

# _FORMAT_EX_PARAMETERS structure


## -description


Contains information used in formatting a contiguous set of disk tracks. It is used by the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff559448">IOCTL_DISK_FORMAT_TRACKS_EX</a> control code.


## -struct-fields




### -field MediaType

The media type. For a list of values, see 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff562216">MEDIA_TYPE</a>.


### -field StartCylinderNumber

The cylinder number at which to begin the format.


### -field EndCylinderNumber

The cylinder number at which to end the format.


### -field StartHeadNumber

The beginning head location. 


### -field EndHeadNumber

The ending head location.


### -field FormatGapLength

The length of the gap between two successive sectors on a track.


### -field SectorsPerTrack

The number of sectors in each track.


### -field SectorNumber

An array of values specifying the sector numbers of the sectors to be included in the track to be formatted.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff559448">IOCTL_DISK_FORMAT_TRACKS_EX</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff562216">MEDIA_TYPE</a>
 

 

