---
UID: NS:ntmsapi._NTMS_DRIVEINFORMATIONA
title: NTMS_DRIVEINFORMATIONA (ntmsapi.h)
description: The NTMS_DRIVEINFORMATION structure defines properties specific to a drive object. (ANSI)
helpviewer_keywords: ["NTMS_DRIVEINFORMATION","NTMS_DRIVEINFORMATION structure [Files]","NTMS_DRIVEINFORMATIONA","NTMS_DRIVEINFORMATIONW","NTMS_DRIVESTATE_BEING_CLEANED","NTMS_DRIVESTATE_DISMOUNTABLE","NTMS_DRIVESTATE_DISMOUNTED","NTMS_DRIVESTATE_LOADED","NTMS_DRIVESTATE_MOUNTED","NTMS_DRIVESTATE_UNLOADED","_NTMS_DRIVEINFORMATIONA","_NTMS_DRIVEINFORMATIONW","_zaw_ntms_driveinformation","base.ntms_driveinformation","fs.ntms_driveinformation","ntmsapi/NTMS_DRIVEINFORMATION"]
old-location: fs\ntms_driveinformation.htm
tech.root: fs
ms.assetid: a095a8f1-a059-4aed-88da-a139286993b5
ms.date: 12/05/2018
ms.keywords: NTMS_DRIVEINFORMATION, NTMS_DRIVEINFORMATION structure [Files], NTMS_DRIVEINFORMATIONA, NTMS_DRIVEINFORMATIONW, NTMS_DRIVESTATE_BEING_CLEANED, NTMS_DRIVESTATE_DISMOUNTABLE, NTMS_DRIVESTATE_DISMOUNTED, NTMS_DRIVESTATE_LOADED, NTMS_DRIVESTATE_MOUNTED, NTMS_DRIVESTATE_UNLOADED, _NTMS_DRIVEINFORMATIONA, _NTMS_DRIVEINFORMATIONW, _zaw_ntms_driveinformation, base.ntms_driveinformation, fs.ntms_driveinformation, ntmsapi/NTMS_DRIVEINFORMATION
req.header: ntmsapi.h
req.include-header: 
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
req.typenames: NTMS_DRIVEINFORMATIONA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NTMS_DRIVEINFORMATIONA
 - ntmsapi/_NTMS_DRIVEINFORMATIONA
 - NTMS_DRIVEINFORMATIONA
 - ntmsapi/NTMS_DRIVEINFORMATIONA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntmsapi.h
api_name:
 - NTMS_DRIVEINFORMATION
 - NTMS_DRIVEINFORMATIONA
 - NTMS_DRIVEINFORMATIONW
---

# NTMS_DRIVEINFORMATIONA structure


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>NTMS_DRIVEINFORMATION</b> structure defines properties specific to a drive object.

## -struct-fields

### -field Number

Number of the drive in the library. This is set zero or one relative the value based on the drive numbering system of the device. Some changers number drives beginning with zero, and some changers begin with one.

### -field State

State of the drive. This can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_DRIVESTATE_BEING_CLEANED"></a><a id="ntms_drivestate_being_cleaned"></a><dl>
<dt><b>NTMS_DRIVESTATE_BEING_CLEANED</b></dt>
</dl>
</td>
<td width="60%">
The drive is being cleaned and is unavailable.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_DRIVESTATE_DISMOUNTABLE"></a><a id="ntms_drivestate_dismountable"></a><dl>
<dt><b>NTMS_DRIVESTATE_DISMOUNTABLE</b></dt>
</dl>
</td>
<td width="60%">
If a library is set for lazy dismounts, the medium might be left in the library's drive on a dismount. RSM can satisfy mount requests for loaded and dismounted drives.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_DRIVESTATE_DISMOUNTED"></a><a id="ntms_drivestate_dismounted"></a><dl>
<dt><b>NTMS_DRIVESTATE_DISMOUNTED</b></dt>
</dl>
</td>
<td width="60%">
No medium in the drive.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_DRIVESTATE_LOADED"></a><a id="ntms_drivestate_loaded"></a><dl>
<dt><b>NTMS_DRIVESTATE_LOADED</b></dt>
</dl>
</td>
<td width="60%">
The medium is mounted in the drive and is loaded for read and write access.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_DRIVESTATE_MOUNTED"></a><a id="ntms_drivestate_mounted"></a><dl>
<dt><b>NTMS_DRIVESTATE_MOUNTED</b></dt>
</dl>
</td>
<td width="60%">
The medium is mounted in the drive but is not ready for read and write access. This is a temporary state that is used while a drive is waiting for spindle synchronization or loading tape media into the head mechanism.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_DRIVESTATE_UNLOADED"></a><a id="ntms_drivestate_unloaded"></a><dl>
<dt><b>NTMS_DRIVESTATE_UNLOADED</b></dt>
</dl>
</td>
<td width="60%">
The medium has been dismounted by the drive and is ready to be opened. This state indicates that the spindle has stopped or a tape media has been returned to the tape cartridge.

</td>
</tr>
</table>

### -field DriveType

Unique identifier of the drive type object containing the attributes for the drive.

### -field szDeviceName

Name of the device used to access the drive. For a tape drive this contains the device name \\.\tape0 or \\.\tape1. Other devices provide the name of a SCSI disk drive or the root of a file system that currently has the device mounted (raw, NTFS, FAT and so forth).

### -field szSerialNumber

Serial number for the drive represented as a string. Devices that do not support serial numbers report NULL for this member.

### -field szRevision

Revision for the drive represented as a string.

### -field ScsiPort

SCSI host adapter to which the drive is connected.

### -field ScsiBus

SCSI bus to which the drive is connected.

### -field ScsiTarget

SCSI target ID for the drive.

### -field ScsiLun

SCSI logical unit ID for the drive.

### -field dwMountCount

Number of times the drive has had a medium mounted to it. If the drive supports the reporting of a unique serial number, this value is the number of times the drive has been mounted since it was installed. If the drive does not support the reporting of serial numbers, this member reflects the number of mounts to all of the drives at that location.

### -field LastCleanedTs

Last time the drive was cleaned.

### -field SavedPartitionId

Partition identifier of the medium that is in the drive. If this value is NULL and the drive is found to be full, the media was loaded by a user and needs to be classified.

### -field Library

Unique identifier of the library that contains the drive.

### -field Reserved

Reserved.

### -field dwDeferDismountDelay

Minimum number of seconds a medium will remain in a drive of a library after a deferred dismount has been performed. The default is 5 minutes. This member does not apply to stand-alone libraries. This member is writable.

## -remarks

The 
<b>NTMS_DRIVEINFORMATION</b> structure is included in the 
<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_objectinformationa">NTMS_OBJECTINFORMATION</a> structure.





> [!NOTE]
> The ntmsapi.h header defines NTMS_DRIVEINFORMATION as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_objectinformationa">NTMS_OBJECTINFORMATION</a>
