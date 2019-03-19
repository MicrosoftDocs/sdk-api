---
UID: NS:winioctl._FORMAT_EX_PARAMETERS
title: FORMAT_EX_PARAMETERS (winioctl.h)
author: windows-sdk-content
description: Contains information used in formatting a contiguous set of disk tracks. It is used by the IOCTL_DISK_FORMAT_TRACKS_EX control code.
old-location: fs\format_ex_parameters_str.htm
tech.root: FileIO
ms.assetid: e508106c-a77a-476f-ba71-ea8f9a2d94d6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PFORMAT_EX_PARAMETERS, FORMAT_EX_PARAMETERS, FORMAT_EX_PARAMETERS structure [Files], PFORMAT_EX_PARAMETERS, PFORMAT_EX_PARAMETERS structure pointer [Files], _win32_format_ex_parameters_str, base.format_ex_parameters_str, fs.format_ex_parameters_str, winioctl/FORMAT_EX_PARAMETERS, winioctl/PFORMAT_EX_PARAMETERS"
ms.topic: struct
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - WinIoCtl.h
api_name:
 - FORMAT_EX_PARAMETERS
product: Windows
targetos: Windows
req.typenames: FORMAT_EX_PARAMETERS, *PFORMAT_EX_PARAMETERS
req.redist: 
---

# FORMAT_EX_PARAMETERS structure


## -description


Contains information used in formatting a contiguous set of disk tracks. It is used by the 
<a href="https://msdn.microsoft.com/50ca069e-efc5-46d8-bf8f-ff44e1593a76">IOCTL_DISK_FORMAT_TRACKS_EX</a> control code.


## -struct-fields




### -field MediaType

The media type. For a list of values, see 
<a href="https://msdn.microsoft.com/183cf8fc-c17b-4def-b590-0aa4b67488f6">MEDIA_TYPE</a>.


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




<a href="https://msdn.microsoft.com/50ca069e-efc5-46d8-bf8f-ff44e1593a76">IOCTL_DISK_FORMAT_TRACKS_EX</a>



<a href="https://msdn.microsoft.com/183cf8fc-c17b-4def-b590-0aa4b67488f6">MEDIA_TYPE</a>
 

 

