---
UID: NS:winioctl._PLEX_READ_DATA_REQUEST
title: "_PLEX_READ_DATA_REQUEST"
author: windows-sdk-content
description: Indicates the range of the read operation to perform and the plex from which to read.
old-location: fs\plex_read_data_request_str.htm
old-project: fileio
ms.assetid: efabc8f3-1596-4a6a-86a3-ecd5b3d934d5
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PPLEX_READ_DATA_REQUEST, PLEX_READ_DATA_REQUEST, PLEX_READ_DATA_REQUEST structure [Files], PPLEX_READ_DATA_REQUEST, PPLEX_READ_DATA_REQUEST structure pointer [Files], _PLEX_READ_DATA_REQUEST, _win32_plex_read_data_request_str, base.plex_read_data_request_str, fs.plex_read_data_request_str, winioctl/PLEX_READ_DATA_REQUEST, winioctl/PPLEX_READ_DATA_REQUEST"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winioctl.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: PLEX_READ_DATA_REQUEST, *PPLEX_READ_DATA_REQUEST
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - PLEX_READ_DATA_REQUEST
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _PLEX_READ_DATA_REQUEST structure


## -description


Indicates the range of the read operation to perform and the plex from which to read.


## -struct-fields




### -field ByteOffset

The offset of the range to be read. The offset can be the virtual offset to a file or volume. File offsets should be cluster aligned and volume offsets should be sector aligned.
					


### -field ByteLength

The length of the range to be read. The maximum value is 64 KB. 


### -field PlexNumber

The plex from which to read. A value of zero indicates the primary copy, a value of one indicates the secondary copy, and so on.


## -see-also




<a href="https://msdn.microsoft.com/f2cddd4d-cb58-484c-9a85-274b88ec4ece">FSCTL_READ_FROM_PLEX</a>
 

 

