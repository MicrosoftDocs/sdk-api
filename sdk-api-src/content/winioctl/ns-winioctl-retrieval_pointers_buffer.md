---
UID: NS:winioctl.RETRIEVAL_POINTERS_BUFFER
title: RETRIEVAL_POINTERS_BUFFER
description: Contains the output for the FSCTL_GET_RETRIEVAL_POINTERS control code.
helpviewer_keywords: ["*PRETRIEVAL_POINTERS_BUFFER","PRETRIEVAL_POINTERS_BUFFER","PRETRIEVAL_POINTERS_BUFFER structure pointer [Files]","RETRIEVAL_POINTERS_BUFFER","RETRIEVAL_POINTERS_BUFFER structure [Files]","_win32_retrieval_pointers_buffer_str","base.retrieval_pointers_buffer_str","fs.retrieval_pointers_buffer_str","winioctl/PRETRIEVAL_POINTERS_BUFFER","winioctl/RETRIEVAL_POINTERS_BUFFER"]
old-location: fs\retrieval_pointers_buffer_str.htm
tech.root: fs
ms.assetid: ce6ac9c7-6fce-4019-83cf-2f0250d12339
ms.date: 12/05/2018
ms.keywords: '*PRETRIEVAL_POINTERS_BUFFER, PRETRIEVAL_POINTERS_BUFFER, PRETRIEVAL_POINTERS_BUFFER structure pointer [Files], RETRIEVAL_POINTERS_BUFFER, RETRIEVAL_POINTERS_BUFFER structure [Files], _win32_retrieval_pointers_buffer_str, base.retrieval_pointers_buffer_str, fs.retrieval_pointers_buffer_str, winioctl/PRETRIEVAL_POINTERS_BUFFER, winioctl/RETRIEVAL_POINTERS_BUFFER'
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
req.typenames: RETRIEVAL_POINTERS_BUFFER, *PRETRIEVAL_POINTERS_BUFFER
req.redist: 
f1_keywords:
 - RETRIEVAL_POINTERS_BUFFER
 - winioctl/RETRIEVAL_POINTERS_BUFFER
 - PRETRIEVAL_POINTERS_BUFFER
 - winioctl/PRETRIEVAL_POINTERS_BUFFER
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
 - RETRIEVAL_POINTERS_BUFFER
---

# RETRIEVAL_POINTERS_BUFFER structure


## -description

Contains the output for the 
<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_retrieval_pointers">FSCTL_GET_RETRIEVAL_POINTERS</a> control code.

## -struct-fields

### -field ExtentCount

The count of elements in the <b>Extents</b> array.

### -field StartingVcn

The starting VCN returned by the function call. This is not necessarily the VCN requested by the function call, as the file system driver may round down to the first VCN of the extent in which the requested starting VCN is found.

### -field NextVcn

### -field Lcn

### -field Extents

Array of <b>Extents</b> structures. For the number of members in the array, see <b>ExtentCount</b>. Each member of the array has the following members.



#### NextVcn

The VCN at which the next extent begins. This value minus either <b>StartingVcn</b> (for the first <b>Extents</b> array member) or the <b>NextVcn</b> of the previous member of the array (for all other <b>Extents</b> array members) is the length, in clusters, of the current extent. The length is an input to the <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_move_file">FSCTL_MOVE_FILE</a> operation.



#### Lcn

The LCN at which the current extent begins on the volume. This value is an input to the <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_move_file">FSCTL_MOVE_FILE</a> operation. On the NTFS file system, the value (LONGLONG) –1 indicates either a compression unit that is partially allocated, or an unallocated region of a sparse file.

## -see-also

<a href="/windows/desktop/FileIO/defragmenting-files">Defragmentation</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_retrieval_pointers">FSCTL_GET_RETRIEVAL_POINTERS</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_move_file">FSCTL_MOVE_FILE</a>