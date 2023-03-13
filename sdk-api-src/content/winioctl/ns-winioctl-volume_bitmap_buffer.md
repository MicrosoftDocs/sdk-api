---
UID: NS:winioctl.VOLUME_BITMAP_BUFFER
title: VOLUME_BITMAP_BUFFER
description: Represents the occupied and available clusters on a disk.
helpviewer_keywords: ["*PVOLUME_BITMAP_BUFFER","PVOLUME_BITMAP_BUFFER","PVOLUME_BITMAP_BUFFER structure pointer [Files]","VOLUME_BITMAP_BUFFER","VOLUME_BITMAP_BUFFER structure [Files]","_win32_volume_bitmap_buffer_str","base.volume_bitmap_buffer_str","fs.volume_bitmap_buffer_str","winioctl/PVOLUME_BITMAP_BUFFER","winioctl/VOLUME_BITMAP_BUFFER"]
old-location: fs\volume_bitmap_buffer_str.htm
tech.root: fs
ms.assetid: 7273f469-bc5e-46b7-b908-59ddb7389c27
ms.date: 12/05/2018
ms.keywords: '*PVOLUME_BITMAP_BUFFER, PVOLUME_BITMAP_BUFFER, PVOLUME_BITMAP_BUFFER structure pointer [Files], VOLUME_BITMAP_BUFFER, VOLUME_BITMAP_BUFFER structure [Files], _win32_volume_bitmap_buffer_str, base.volume_bitmap_buffer_str, fs.volume_bitmap_buffer_str, winioctl/PVOLUME_BITMAP_BUFFER, winioctl/VOLUME_BITMAP_BUFFER'
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
req.typenames: VOLUME_BITMAP_BUFFER, *PVOLUME_BITMAP_BUFFER
req.redist: 
f1_keywords:
 - PVOLUME_BITMAP_BUFFER
 - winioctl/PVOLUME_BITMAP_BUFFER
 - VOLUME_BITMAP_BUFFER
 - winioctl/VOLUME_BITMAP_BUFFER
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
 - VOLUME_BITMAP_BUFFER
---

# VOLUME_BITMAP_BUFFER structure


## -description

Represents the occupied and available clusters on a disk. This structure is the output buffer for the 
<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_volume_bitmap">FSCTL_GET_VOLUME_BITMAP</a> control code.

## -struct-fields

### -field StartingLcn

Starting LCN requested as an input to the operation.

### -field BitmapSize

The number of clusters on the volume, starting from the starting LCN returned in the <b>StartingLcn</b> member of this structure. See the following Remarks section for details.

### -field Buffer

Array of bytes containing the bitmap that the operation returns. The bitmap is bitwise from bit zero of the bitmap to the end. Thus, starting at the requested cluster, the bitmap goes from bit 0 of byte 0, bit 1 of byte 0 ... bit 7 of byte 0, bit 0 of byte 1, and so on. The value 1 indicates that the cluster is allocated (in use). The value 0 indicates that the cluster is not allocated (free).

## -remarks

The <b>BitmapSize</b> member is the number of clusters on the volume starting from the starting LCN returned in the <b>StartingLcn</b> member of this structure. For example, suppose there are 0xD3F7 clusters on the volume. If you start the bitmap query at LCN 0xA007, then both the FAT and NTFS file systems will round down the returned starting LCN to LCN 0xA000. The value returned in the <b>BitmapSize</b> member will be (0xD3F7 – 0xA000), or 0x33F7.

## -see-also

<a href="/windows/desktop/FileIO/defragmenting-files">Defragmentation</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_volume_bitmap">FSCTL_GET_VOLUME_BITMAP</a>

