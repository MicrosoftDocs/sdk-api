---
UID: NS:winioctl.STARTING_VCN_INPUT_BUFFER
title: STARTING_VCN_INPUT_BUFFER
description: Contains the starting VCN to the FSCTL_GET_RETRIEVAL_POINTERS control code.
helpviewer_keywords: ["*PSTARTING_VCN_INPUT_BUFFER","PSTARTING_VCN_INPUT_BUFFER","PSTARTING_VCN_INPUT_BUFFER structure pointer [Files]","STARTING_VCN_INPUT_BUFFER","STARTING_VCN_INPUT_BUFFER structure [Files]","_win32_starting_vcn_input_buffer_str","base.starting_vcn_input_buffer_str","fs.starting_vcn_input_buffer_str","winioctl/PSTARTING_VCN_INPUT_BUFFER","winioctl/STARTING_VCN_INPUT_BUFFER"]
old-location: fs\starting_vcn_input_buffer_str.htm
tech.root: fs
ms.assetid: b07668f9-b984-41cc-9545-8f4f9bff3682
ms.date: 12/05/2018
ms.keywords: '*PSTARTING_VCN_INPUT_BUFFER, PSTARTING_VCN_INPUT_BUFFER, PSTARTING_VCN_INPUT_BUFFER structure pointer [Files], STARTING_VCN_INPUT_BUFFER, STARTING_VCN_INPUT_BUFFER structure [Files], _win32_starting_vcn_input_buffer_str, base.starting_vcn_input_buffer_str, fs.starting_vcn_input_buffer_str, winioctl/PSTARTING_VCN_INPUT_BUFFER, winioctl/STARTING_VCN_INPUT_BUFFER'
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
targetos: Windows
req.typenames: STARTING_VCN_INPUT_BUFFER, *PSTARTING_VCN_INPUT_BUFFER
req.redist: 
f1_keywords:
 - PSTARTING_VCN_INPUT_BUFFER
 - winioctl/PSTARTING_VCN_INPUT_BUFFER
 - STARTING_VCN_INPUT_BUFFER
 - winioctl/STARTING_VCN_INPUT_BUFFER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - STARTING_VCN_INPUT_BUFFER
---

# STARTING_VCN_INPUT_BUFFER structure


## -description

Contains the starting VCN to the 
<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_retrieval_pointers">FSCTL_GET_RETRIEVAL_POINTERS</a> control code.

## -struct-fields

### -field StartingVcn

The VCN at which 
the operation will begin enumerating extents in the file. This value may be rounded down to the first VCN of the extent in which the specified extent is found.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa364407(v=vs.85)">Defragmentation</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_retrieval_pointers">FSCTL_GET_RETRIEVAL_POINTERS</a>

