---
UID: NS:winioctl._FILE_MAKE_COMPATIBLE_BUFFER
title: "_FILE_MAKE_COMPATIBLE_BUFFER"
author: windows-sdk-content
description: Specifies the disc to close the current session for. This control code is used for UDF file systems. This structure is used for input when calling FSCTL_MAKE_MEDIA_COMPATIBLE.
old-location: fs\file_make_compatible_buffer.htm
old-project: FileIO
ms.assetid: 1c7b1958-099f-404d-a060-99efc543a3c0
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: "*PFILE_MAKE_COMPATIBLE_BUFFER, FILE_MAKE_COMPATIBLE_BUFFER, FILE_MAKE_COMPATIBLE_BUFFER structure [Files], PFILE_MAKE_COMPATIBLE_BUFFER, PFILE_MAKE_COMPATIBLE_BUFFER structure pointer [Files], _FILE_MAKE_COMPATIBLE_BUFFER, fs.file_make_compatible_buffer, winioctl/FILE_MAKE_COMPATIBLE_BUFFER, winioctl/PFILE_MAKE_COMPATIBLE_BUFFER"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: FILE_MAKE_COMPATIBLE_BUFFER, *PFILE_MAKE_COMPATIBLE_BUFFER
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - FILE_MAKE_COMPATIBLE_BUFFER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _FILE_MAKE_COMPATIBLE_BUFFER structure


## -description


Specifies the disc to close the current session for. This control code is used for UDF file systems. This structure is used for input when calling <a href="https://msdn.microsoft.com/bbe58c35-d0da-4c29-a412-a84a138dc9fb">FSCTL_MAKE_MEDIA_COMPATIBLE</a>.


## -struct-fields




### -field CloseDisc

If <b>TRUE</b>, indicates the media should be finalized. No new data can be appended to the media.


## -see-also




<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/bbe58c35-d0da-4c29-a412-a84a138dc9fb">FSCTL_MAKE_MEDIA_COMPATIBLE</a>
 

 

