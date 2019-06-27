---
UID: NS:winioctl._FORMAT_PARAMETERS
title: FORMAT_PARAMETERS
author: windows-sdk-content
description: Contains information used in formatting a contiguous set of disk tracks.
old-location: fs\format_parameters_str.htm
tech.root: FileIO
ms.assetid: 81fcfd8e-abb9-4c0b-b23d-302aa3645a6f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PFORMAT_PARAMETERS, FORMAT_PARAMETERS, FORMAT_PARAMETERS structure [Files], PFORMAT_PARAMETERS, PFORMAT_PARAMETERS structure pointer [Files], _win32_format_parameters_str, base.format_parameters_str, fs.format_parameters_str, winioctl/FORMAT_PARAMETERS, winioctl/PFORMAT_PARAMETERS"
ms.topic: struct
f1_keywords: 
 - "winioctl/FORMAT_PARAMETERS"
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
 - FORMAT_PARAMETERS
product: Windows
targetos: Windows
req.typenames: FORMAT_PARAMETERS, *PFORMAT_PARAMETERS
req.redist: 
---

# FORMAT_PARAMETERS structure


## -description


Contains information used in formatting a contiguous set of disk tracks. It is used by the 
<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_format_tracks">IOCTL_DISK_FORMAT_TRACKS</a> control code. 


## -struct-fields




### -field MediaType

The media type. For a list of values, see 
<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ne-winioctl-_media_type">MEDIA_TYPE</a>.


### -field StartCylinderNumber

The cylinder number at which to begin the format.


### -field EndCylinderNumber

The cylinder number at which to end the format.


### -field StartHeadNumber

The beginning head location. 


### -field EndHeadNumber

The ending head location.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_format_tracks">IOCTL_DISK_FORMAT_TRACKS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ne-winioctl-_media_type">MEDIA_TYPE</a>
 

 

