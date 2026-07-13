---
UID: NS:winioctl.NTFS_EXTENDED_VOLUME_DATA
title: NTFS_EXTENDED_VOLUME_DATA
description: Represents volume data.N
helpviewer_keywords: ["*PNTFS_EXTENDED_VOLUME_DATA","NTFS_EXTENDED_VOLUME_DATA","NTFS_VOLUME_DATA_BUFFER","NTFS_VOLUME_DATA_BUFFER structure [Files]","PNTFS_VOLUME_DATA_BUFFER","PNTFS_VOLUME_DATA_BUFFER structure pointer [Files]","_win32_ntfs_volume_data_buffer_str","base.ntfs_volume_data_buffer_str","fs.ntfs_volume_data_buffer_str","winioctl/NTFS_VOLUME_DATA_BUFFER","winioctl/PNTFS_VOLUME_DATA_BUFFER"]
old-location: fs\ntfs_volume_data_buffer_str.htm
tech.root: fs
ms.assetid: 9ca0fe72-162c-4d75-a2f3-e1c7c0b0152a
ms.date: 12/05/2018
ms.keywords: '*PNTFS_EXTENDED_VOLUME_DATA, NTFS_EXTENDED_VOLUME_DATA, NTFS_VOLUME_DATA_BUFFER, NTFS_VOLUME_DATA_BUFFER structure [Files], PNTFS_VOLUME_DATA_BUFFER, PNTFS_VOLUME_DATA_BUFFER structure pointer [Files], _win32_ntfs_volume_data_buffer_str, base.ntfs_volume_data_buffer_str, fs.ntfs_volume_data_buffer_str, winioctl/NTFS_VOLUME_DATA_BUFFER, winioctl/PNTFS_VOLUME_DATA_BUFFER'
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
req.typenames: NTFS_EXTENDED_VOLUME_DATA, *PNTFS_EXTENDED_VOLUME_DATA
req.redist: 
f1_keywords:
 - PNTFS_EXTENDED_VOLUME_DATA
 - winioctl/PNTFS_EXTENDED_VOLUME_DATA
 - NTFS_EXTENDED_VOLUME_DATA
 - winioctl/NTFS_EXTENDED_VOLUME_DATA
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
 - NTFS_EXTENDED_VOLUME_DATA
---

# NTFS_EXTENDED_VOLUME_DATA structure


## -description

Represents volume data.  This structure is passed to the 
<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data">FSCTL_GET_NTFS_VOLUME_DATA</a> control code.

## -struct-fields

### -field ByteCount

### -field MajorVersion

### -field MinorVersion

### -field BytesPerPhysicalSector

### -field LfsMajorVersion

### -field LfsMinorVersion

### -field MaxDeviceTrimExtentCount

### -field MaxDeviceTrimByteCount

### -field MaxVolumeTrimExtentCount

### -field MaxVolumeTrimByteCount

 




#### - BytesPerCluster

The number of bytes in a cluster on the specified volume. This value is also known as the cluster factor.


#### - BytesPerFileRecordSegment

The number of bytes in a file record segment.


#### - BytesPerSector

The number of bytes in a sector on the specified volume.


#### - ClustersPerFileRecordSegment

The number of clusters in a file record segment.


#### - FreeClusters

The number of free clusters in the specified volume.


#### - Mft2StartLcn

The starting logical cluster number of the master file table mirror.


#### - MftStartLcn

The starting logical cluster number of the master file table.


#### - MftValidDataLength

The length of the master file table, in bytes.


#### - MftZoneEnd

The ending logical cluster number of the master file table zone.


#### - MftZoneStart

The starting logical cluster number of the master file table zone.


#### - NumberSectors

The number of sectors in the specified volume.


#### - TotalClusters

The number of used and free clusters in the specified volume.


#### - TotalReserved

The number of reserved clusters in the specified volume.


#### - VolumeSerialNumber

The serial number of the volume. This is a unique number assigned to the volume media by the operating system.

## -remarks

Reserved clusters are the free clusters reserved for later use by Windows.

The <b>NTFS_VOLUME_DATA_BUFFER</b> structure represents the basic information returned by <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data">FSCTL_GET_NTFS_VOLUME_DATA</a>. For extended volume information,  pass a buffer that is the combined size of the <b>NTFS_VOLUME_DATA_BUFFER</b>  and <b>NTFS_EXTENDED_VOLUME_DATA</b> structures. Upon success, the  buffer returned by <b>FSCTL_GET_NTFS_VOLUME_DATA</b> will contain the information associated with both structures. The <b>NTFS_VOLUME_DATA_BUFFER</b> structure will always be filled starting at the beginning of the buffer, with the <b>NTFS_EXTENDED_VOLUME_DATA</b> structure immediately following. The <b>NTFS_EXTENDED_VOLUME_DATA</b> structure is defined as follows: 
				

<div class="code"><span><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>typedef struct {
    ULONG ByteCount;
    USHORT MajorVersion;
    USHORT MinorVersion;
} NTFS_EXTENDED_VOLUME_DATA, *PNTFS_EXTENDED_VOLUME_DATA;</pre>
</td>
</tr>
</table></span></div>
This structure contains the major and minor version information for an NTFS volume. The <b>ByteCount</b> member will return the total bytes  of the output buffer used for this structure by the call to <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data">FSCTL_GET_NTFS_VOLUME_DATA</a>. This value should be <code>sizeof(NTFS_EXTENDED_VOLUME_DATA)</code> if the buffer passed was large enough to hold it, otherwise the value will be less than <code>sizeof(NTFS_EXTENDED_VOLUME_DATA)</code>.

## -see-also

<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data">FSCTL_GET_NTFS_VOLUME_DATA</a>

