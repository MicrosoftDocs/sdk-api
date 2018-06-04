---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# NTFS_VOLUME_DATA_BUFFER structure


## -description


Represents volume data.  This structure is passed to the 
<a href="https://msdn.microsoft.com/b5690b4f-3967-41d8-bf11-70f8b1da79ad">FSCTL_GET_NTFS_VOLUME_DATA</a> control code.


## -struct-fields




#### - VolumeSerialNumber

The serial number of the volume. This is a unique number assigned to the volume media by the operating system.


#### - NumberSectors

The number of sectors in the specified volume.


#### - TotalClusters

The number of used and free clusters in the specified volume.


#### - FreeClusters

The number of free clusters in the specified volume.


#### - TotalReserved

The number of reserved clusters in the specified volume.


#### - BytesPerSector

The number of bytes in a sector on the specified volume.


#### - BytesPerCluster

The number of bytes in a cluster on the specified volume. This value is also known as the cluster factor.


#### - BytesPerFileRecordSegment

The number of bytes in a file record segment.


#### - ClustersPerFileRecordSegment

The number of clusters in a file record segment.


#### - MftValidDataLength

The length of the master file table, in bytes.


#### - MftStartLcn

The starting logical cluster number of the master file table.


#### - Mft2StartLcn

The starting logical cluster number of the master file table mirror.


#### - MftZoneStart

The starting logical cluster number of the master file table zone.


#### - MftZoneEnd

The ending logical cluster number of the master file table zone.


## -remarks



Reserved clusters are the free clusters reserved for later use by Windows.

The <b>NTFS_VOLUME_DATA_BUFFER</b> structure represents the basic information returned by <a href="https://msdn.microsoft.com/b5690b4f-3967-41d8-bf11-70f8b1da79ad">FSCTL_GET_NTFS_VOLUME_DATA</a>. For extended volume information,  pass a buffer that is the combined size of the <b>NTFS_VOLUME_DATA_BUFFER</b>  and <b>NTFS_EXTENDED_VOLUME_DATA</b> structures. Upon success, the  buffer returned by <b>FSCTL_GET_NTFS_VOLUME_DATA</b> will contain the information associated with both structures. The <b>NTFS_VOLUME_DATA_BUFFER</b> structure will always be filled starting at the beginning of the buffer, with the <b>NTFS_EXTENDED_VOLUME_DATA</b> structure immediately following. The <b>NTFS_EXTENDED_VOLUME_DATA</b> structure is defined as follows: 
				

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
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
This structure contains the major and minor version information for an NTFS volume. The <b>ByteCount</b> member will return the total bytes  of the output buffer used for this structure by the call to <a href="https://msdn.microsoft.com/b5690b4f-3967-41d8-bf11-70f8b1da79ad">FSCTL_GET_NTFS_VOLUME_DATA</a>. This value should be <code>sizeof(NTFS_EXTENDED_VOLUME_DATA)</code> if the buffer passed was large enough to hold it, otherwise the value will be less than <code>sizeof(NTFS_EXTENDED_VOLUME_DATA)</code>.




## -see-also




<a href="https://msdn.microsoft.com/b5690b4f-3967-41d8-bf11-70f8b1da79ad">FSCTL_GET_NTFS_VOLUME_DATA</a>
 

 

