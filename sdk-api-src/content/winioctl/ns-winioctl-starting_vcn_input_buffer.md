---
UID: NS:winioctl.STARTING_VCN_INPUT_BUFFER
title: STARTING_VCN_INPUT_BUFFER
author: windows-sdk-content
description: Contains the starting VCN to the FSCTL_GET_RETRIEVAL_POINTERS control code.
old-location: fs\starting_vcn_input_buffer_str.htm
tech.root: fileio
ms.assetid: b07668f9-b984-41cc-9545-8f4f9bff3682
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PSTARTING_VCN_INPUT_BUFFER, PSTARTING_VCN_INPUT_BUFFER, PSTARTING_VCN_INPUT_BUFFER structure pointer [Files], STARTING_VCN_INPUT_BUFFER, STARTING_VCN_INPUT_BUFFER structure [Files], _win32_starting_vcn_input_buffer_str, base.starting_vcn_input_buffer_str, fs.starting_vcn_input_buffer_str, winioctl/PSTARTING_VCN_INPUT_BUFFER, winioctl/STARTING_VCN_INPUT_BUFFER"
ms.prod: windows
ms.technology: windows-sdk
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
 - STARTING_VCN_INPUT_BUFFER
product: Windows
targetos: Windows
req.typenames: STARTING_VCN_INPUT_BUFFER, *PSTARTING_VCN_INPUT_BUFFER
req.redist: 
---

# STARTING_VCN_INPUT_BUFFER structure


## -description


Contains the starting VCN to the 
<a href="https://msdn.microsoft.com/002f6703-8db3-4034-a79f-3fa9c4159115">FSCTL_GET_RETRIEVAL_POINTERS</a> control code.


## -struct-fields




### -field StartingVcn

The VCN at which 
the operation will begin enumerating extents in the file. This value may be rounded down to the first VCN of the extent in which the specified extent is found.


## -see-also




<a href="https://msdn.microsoft.com/a35dbd6e-1344-4694-9760-7bc3d33196e5">Defragmentation</a>



<a href="https://msdn.microsoft.com/002f6703-8db3-4034-a79f-3fa9c4159115">FSCTL_GET_RETRIEVAL_POINTERS</a>
 

 

