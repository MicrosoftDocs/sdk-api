---
UID: NS:winioctl._FORMAT_PARAMETERS
title: FORMAT_PARAMETERS (winioctl.h)
author: windows-sdk-content
description: Contains information used in formatting a contiguous set of disk tracks.
old-location: fs\format_parameters_str.htm
tech.root: FileIO
ms.assetid: 81fcfd8e-abb9-4c0b-b23d-302aa3645a6f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PFORMAT_PARAMETERS, FORMAT_PARAMETERS, FORMAT_PARAMETERS structure [Files], PFORMAT_PARAMETERS, PFORMAT_PARAMETERS structure pointer [Files], _win32_format_parameters_str, base.format_parameters_str, fs.format_parameters_str, winioctl/FORMAT_PARAMETERS, winioctl/PFORMAT_PARAMETERS"
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
 - FORMAT_PARAMETERS
product: Windows
targetos: Windows
req.typenames: FORMAT_PARAMETERS, *PFORMAT_PARAMETERS
req.redist: 
---

# FORMAT_PARAMETERS structure


## -description


Contains information used in formatting a contiguous set of disk tracks. It is used by the 
<a href="https://msdn.microsoft.com/9d6e0865-4b4d-4334-855b-3fbd26832591">IOCTL_DISK_FORMAT_TRACKS</a> control code. 


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


## -see-also




<a href="https://msdn.microsoft.com/9d6e0865-4b4d-4334-855b-3fbd26832591">IOCTL_DISK_FORMAT_TRACKS</a>



<a href="https://msdn.microsoft.com/183cf8fc-c17b-4def-b590-0aa4b67488f6">MEDIA_TYPE</a>
 

 

