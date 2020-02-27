---
UID: NS:winioctl.__unnamed_struct_4
title: STARTING_LCN_INPUT_BUFFER
description: Contains the starting LCN to the FSCTL_GET_VOLUME_BITMAP control code.
old-location: fs\starting_lcn_input_buffer_str.htm
tech.root: FileIO
ms.assetid: 94bdb166-fe75-4851-9dbb-a1a1f5836675
ms.date: 12/05/2018
ms.keywords: '*PSTARTING_LCN_INPUT_BUFFER, PSTARTING_LCN_INPUT_BUFFER, PSTARTING_LCN_INPUT_BUFFER structure pointer [Files], STARTING_LCN_INPUT_BUFFER, STARTING_LCN_INPUT_BUFFER structure [Files], _win32_starting_lcn_input_buffer_str, base.starting_lcn_input_buffer_str, fs.starting_lcn_input_buffer_str, winioctl/PSTARTING_LCN_INPUT_BUFFER, winioctl/STARTING_LCN_INPUT_BUFFER'
f1_keywords:
- winioctl/STARTING_LCN_INPUT_BUFFER
dev_langs:
- c++
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
- STARTING_LCN_INPUT_BUFFER
targetos: Windows
req.typenames: STARTING_LCN_INPUT_BUFFER, *PSTARTING_LCN_INPUT_BUFFER
req.redist: 
---

# STARTING_LCN_INPUT_BUFFER structure


## -description


Contains the starting LCN to the 
<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_volume_bitmap">FSCTL_GET_VOLUME_BITMAP</a> control code.


## -struct-fields




### -field StartingLcn

The LCN from which the operation should start when describing a bitmap. This member will be rounded down to a file-system-dependent rounding boundary, and that value will be returned. Its  value should be an integral multiple of eight.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/FileIO/defragmenting-files">Defragmentation</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_volume_bitmap">FSCTL_GET_VOLUME_BITMAP</a>
 

 

