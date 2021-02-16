---
UID: NS:winioctl._FSCTL_GET_INTEGRITY_INFORMATION_BUFFER
title: FSCTL_GET_INTEGRITY_INFORMATION_BUFFER
description: Contains the integrity information for a file or directory.
helpviewer_keywords: ["*PFSCTL_GET_INTEGRITY_INFORMATION_BUFFER","CHECKSUM_TYPE_CRC64","CHECKSUM_TYPE_NONE","FSCTL_GET_INTEGRITY_INFORMATION_BUFFER","FSCTL_GET_INTEGRITY_INFORMATION_BUFFER structure [Files]","FSCTL_INTEGRITY_FLAG_CHECKSUM_ENFORCEMENT_OFF","PFSCTL_GET_INTEGRITY_INFORMATION_BUFFER","PFSCTL_GET_INTEGRITY_INFORMATION_BUFFER structure pointer [Files]","fs.fsctl_get_integrity_information_buffer","winioctl/FSCTL_GET_INTEGRITY_INFORMATION_BUFFER","winioctl/PFSCTL_GET_INTEGRITY_INFORMATION_BUFFER"]
old-location: fs\fsctl_get_integrity_information_buffer.htm
tech.root: fs
ms.assetid: ab87f987-b734-4ad0-af16-1ba967db48d7
ms.date: 12/05/2018
ms.keywords: '*PFSCTL_GET_INTEGRITY_INFORMATION_BUFFER, CHECKSUM_TYPE_CRC64, CHECKSUM_TYPE_NONE, FSCTL_GET_INTEGRITY_INFORMATION_BUFFER, FSCTL_GET_INTEGRITY_INFORMATION_BUFFER structure [Files], FSCTL_INTEGRITY_FLAG_CHECKSUM_ENFORCEMENT_OFF, PFSCTL_GET_INTEGRITY_INFORMATION_BUFFER, PFSCTL_GET_INTEGRITY_INFORMATION_BUFFER structure pointer [Files], fs.fsctl_get_integrity_information_buffer, winioctl/FSCTL_GET_INTEGRITY_INFORMATION_BUFFER, winioctl/PFSCTL_GET_INTEGRITY_INFORMATION_BUFFER'
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: FSCTL_GET_INTEGRITY_INFORMATION_BUFFER, *PFSCTL_GET_INTEGRITY_INFORMATION_BUFFER
req.redist: 
f1_keywords:
 - _FSCTL_GET_INTEGRITY_INFORMATION_BUFFER
 - winioctl/_FSCTL_GET_INTEGRITY_INFORMATION_BUFFER
 - PFSCTL_GET_INTEGRITY_INFORMATION_BUFFER
 - winioctl/PFSCTL_GET_INTEGRITY_INFORMATION_BUFFER
 - FSCTL_GET_INTEGRITY_INFORMATION_BUFFER
 - winioctl/FSCTL_GET_INTEGRITY_INFORMATION_BUFFER
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
 - FSCTL_GET_INTEGRITY_INFORMATION_BUFFER
---

# FSCTL_GET_INTEGRITY_INFORMATION_BUFFER structure


## -description

Contains the integrity information for a file or directory. Returned from the <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_integrity_information">FSCTL_GET_INTEGRITY_INFORMATION</a> control code.

## -struct-fields

### -field ChecksumAlgorithm

The checksum algorithm used.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CHECKSUM_TYPE_NONE"></a><a id="checksum_type_none"></a><dl>
<dt><b>CHECKSUM_TYPE_NONE</b></dt>
<dt>0x0000</dt>
</dl>
</td>
<td width="60%">
The file or directory is not configured to use integrity.

</td>
</tr>
<tr>
<td width="40%"><a id="CHECKSUM_TYPE_CRC64"></a><a id="checksum_type_crc64"></a><dl>
<dt><b>CHECKSUM_TYPE_CRC64</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
The file or directory uses a CRC64 checksum to provide integrity.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>3–0xffff</dt>
</dl>
</td>
<td width="60%">
Reserved for future use.

</td>
</tr>
</table>

### -field Reserved

Reserved for future use.  Set to 0.

### -field Flags

Contains one or more flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FSCTL_INTEGRITY_FLAG_CHECKSUM_ENFORCEMENT_OFF"></a><a id="fsctl_integrity_flag_checksum_enforcement_off"></a><dl>
<dt><b>FSCTL_INTEGRITY_FLAG_CHECKSUM_ENFORCEMENT_OFF</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
If set, the checksum enforcement is disabled.

</td>
</tr>
</table>

### -field ChecksumChunkSizeInBytes

Size in bytes of the chunks used to calculate checksums.

### -field ClusterSizeInBytes

Size in bytes of a cluster for this volume. This value must be a power of 2, must be greater than or equal 
      to the sector size of the underlying hardware and must be a power of 2 multiple of the sector size.

## -see-also

<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_integrity_information">FSCTL_GET_INTEGRITY_INFORMATION</a>



<a href="/windows/win32/api/winioctl/ns-winioctl-fsctl_set_integrity_information_buffer">FSCTL_SET_INTEGRITY_INFORMATION_BUFFER</a>



<a href="/windows/desktop/FileIO/volume-management-structures">Volume Management Structures</a>