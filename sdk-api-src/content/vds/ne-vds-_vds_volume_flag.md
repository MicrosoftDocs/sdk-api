---
UID: NE:vds._VDS_VOLUME_FLAG
title: "_VDS_VOLUME_FLAG"
author: windows-sdk-content
description: Defines the set of valid flags for a volume object.
old-location: base\vds_volume_flag.htm
tech.root: VDS
ms.assetid: 3a59cc61-1efe-4027-9aca-a785a5cfaef5
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: VDS_VF_ACTIVE, VDS_VF_BOOT_VOLUME, VDS_VF_CAN_EXTEND, VDS_VF_CAN_SHRINK, VDS_VF_CRASHDUMP, VDS_VF_DIRTY, VDS_VF_FAT32_NOT_SUPPORTED, VDS_VF_FAT_NOT_SUPPORTED, VDS_VF_FORMATTING, VDS_VF_FVE_ENABLED, VDS_VF_HIBERNATION, VDS_VF_HIDDEN, VDS_VF_INSTALLABLE, VDS_VF_LBN_REMAP_ENABLED, VDS_VF_NOT_FORMATTABLE, VDS_VF_NO_DEFAULT_DRIVE_LETTER, VDS_VF_NTFS_NOT_SUPPORTED, VDS_VF_PAGEFILE, VDS_VF_PERMANENTLY_DISMOUNTED, VDS_VF_PERMANENT_DISMOUNT_SUPPORTED, VDS_VF_READONLY, VDS_VF_SHADOW_COPY, VDS_VF_SYSTEM_VOLUME, VDS_VOLUME_FLAG, VDS_VOLUME_FLAG enumeration [VDS], _VDS_VOLUME_FLAG, base.vds_volume_flag, vds/VDS_VF_ACTIVE, vds/VDS_VF_BOOT_VOLUME, vds/VDS_VF_CAN_EXTEND, vds/VDS_VF_CAN_SHRINK, vds/VDS_VF_CRASHDUMP, vds/VDS_VF_DIRTY, vds/VDS_VF_FAT32_NOT_SUPPORTED, vds/VDS_VF_FAT_NOT_SUPPORTED, vds/VDS_VF_FORMATTING, vds/VDS_VF_FVE_ENABLED, vds/VDS_VF_HIBERNATION, vds/VDS_VF_HIDDEN, vds/VDS_VF_INSTALLABLE, vds/VDS_VF_LBN_REMAP_ENABLED, vds/VDS_VF_NOT_FORMATTABLE, vds/VDS_VF_NO_DEFAULT_DRIVE_LETTER, vds/VDS_VF_NTFS_NOT_SUPPORTED, vds/VDS_VF_PAGEFILE, vds/VDS_VF_PERMANENTLY_DISMOUNTED, vds/VDS_VF_PERMANENT_DISMOUNT_SUPPORTED, vds/VDS_VF_READONLY, vds/VDS_VF_SHADOW_COPY, vds/VDS_VF_SYSTEM_VOLUME, vds/VDS_VOLUME_FLAG
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
 - Vds.h
api_name:
 - VDS_VOLUME_FLAG
product: Windows
targetos: Windows
req.typenames: VDS_VOLUME_FLAG
req.redist: 
---

# _VDS_VOLUME_FLAG enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the set of 
   valid flags for a volume object.


## -enum-fields




### -field VDS_VF_SYSTEM_VOLUME

The volume is a system volume.


### -field VDS_VF_BOOT_VOLUME

The volume is the boot volume.


### -field VDS_VF_ACTIVE

The volume is active. That is, the <i>bootIndicator</i> value of the 
      underlying partition is set to true.


### -field VDS_VF_READONLY

The volume has a drive letter and a Mount Manager–assigned volume GUID name, and is enumerated by the <b>FindFirstVolume</b> and <a href="https://msdn.microsoft.com/en-us/library/Aa364431(v=VS.85).aspx">FindNextVolume</a> functions. However, the volume is read-only. This flag does not apply to CD-ROM or DVD devices.


### -field VDS_VF_HIDDEN

The volume does not have a drive letter and a Mount Manager–assigned volume GUID name. The volume is not enumerated by the <b>FindFirstVolume</b> and <a href="https://msdn.microsoft.com/en-us/library/Aa364431(v=VS.85).aspx">FindNextVolume</a> functions. The volume can be opened by using its device name, and the opened volume can be read from or written to. An example of a volume device name is \\?\GLOBALROOT\Device\HarddiskVolumeX. This flag does not apply to CD-ROM or DVD devices.


### -field VDS_VF_CAN_EXTEND

The volume size can be extended.


### -field VDS_VF_CAN_SHRINK

The volume size can be reduced.


### -field VDS_VF_PAGEFILE

The volume contains a pagefile.


### -field VDS_VF_HIBERNATION

The volume contains a hibernation file.


### -field VDS_VF_CRASHDUMP

The volume contains the crash dump file.
      


### -field VDS_VF_INSTALLABLE

VDS creates a hard partition under a dynamic volume that callers can use to install an operating system. Clearing this flag causes the partition to be deleted. This flag can be set or cleared only for dynamic disks; it is always set for basic disks. This flag does not apply to CD-ROM or DVD devices.


### -field VDS_VF_LBN_REMAP_ENABLED

VDS can change the position of the volume on the disk dynamically. This flag is not valid for basic 
      or dynamic volumes and is supported only by some third-party volume managers.


### -field VDS_VF_FORMATTING

The volume is being formatted.


### -field VDS_VF_NOT_FORMATTABLE

The volume cannot be formatted. This flag applies to small portable memory devices, removable 
      devices, CDROM devices, and DVD devices. For CD and DVD devices, this is always set when there is media in the 
      drive, and is not set if there is no media in the drive.


### -field VDS_VF_NTFS_NOT_SUPPORTED

The volume does not support NTFS, but can support other file systems. This flag applies to small 
      portable memory devices, removable devices, CDROM devices, and DVD devices.


### -field VDS_VF_FAT32_NOT_SUPPORTED

The volume does not support FAT32. This flag applies to small portable memory devices, removable 
      devices, CDROM devices, and DVD devices.


### -field VDS_VF_FAT_NOT_SUPPORTED

The volume does not support FAT. This flag applies to small portable memory devices, removable 
      devices, CDROM devices, and DVD devices.


### -field VDS_VF_NO_DEFAULT_DRIVE_LETTER

The operating system does not assign a drive letter automatically the next time the volume is added to the computer. 
      If cleared, the operating system assigns a drive letter to the volume under some conditions. For basic GPT 
      volumes, assigning or removing a drive letter will toggle this flag. This flag does not apply to CD-ROM or DVD devices.

<b>Windows Server 2003:  </b>On dynamic volumes, this flag is always set and cannot be cleared. On basic volumes, it is cleared by default and can be set or cleared only by calling the <a href="https://msdn.microsoft.com/f426b089-6c5f-4ab4-aa92-127e24cb57b1">IVdsVolume::SetFlags</a> or <a href="https://msdn.microsoft.com/970dcd4a-ac06-4e2d-969c-82c5dabd0019">IVdsVolume::ClearFlags</a> method.


### -field VDS_VF_PERMANENTLY_DISMOUNTED

The volume is offline. Volume open will succeed on an offline volume. However, I/O against an offline volume will fail. Assigning an access path, such as a drive letter, to an offline volume causes it to become online. To set this flag, call the <a href="https://msdn.microsoft.com/1ef5a1e6-0e41-4077-9ae8-fe266f2623cc">IVdsVolumeMF::Dismount</a> 
      method, setting the <i>bForce</i> and <i>bPermanent</i> parameters to 
      <b>TRUE</b>. This flag does not apply to CD-ROM or DVD devices.

<b>Windows Server 2003:  </b>Offlining dynamic volumes is not supported.

When a volume is offline, this flag is set in the <b>ulFlags</b> member of the <a href="https://msdn.microsoft.com/3628b312-f830-4a1c-beb7-ad002a94313c">VDS_VOLUME_PROP</a> structure, and the <b>VDS_VS_OFFLINE</b> flag is also set in the <b>status</b> member of the <b>VDS_VOLUME_PROP</b> or <a href="https://msdn.microsoft.com/e99aaead-f5ad-4181-9208-9158e9fac38f">VDS_VOLUME_PROP2</a> structure.<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>The <b>VDS_VS_OFFLINE</b> flag is not supported.




### -field VDS_VF_PERMANENT_DISMOUNT_SUPPORTED

The volume can be taken offline.


### -field VDS_VF_SHADOW_COPY

The volume is a shadow copy of another volume. This flag is set when the shadow copy is created. It is 
      cleared when the shadow copy is broken from the original volume. The <b>VDS_VF_SHADOW_COPY</b> 
      flag is an indication for file system filter driver-based software (such as 
          antivirus programs) to avoid attaching to the 
      volume. The attribute can be used by applications to differentiate shadow copy volumes from production volumes. Applications that 
      perform a Fast Recovery where a shadow copy LUN is made into a non-shadow copy by clearing the read-only and hidden 
      bit will need to clear this bit as well. This flag does not apply to CD-ROM or DVD devices.
      

<b>Windows Server 2003:  </b>This flag is not supported before Windows Server 2003 with SP1.


### -field VDS_VF_FVE_ENABLED

The volume is protected by BitLocker full-volume encryption. This flag does not apply to CD-ROM or DVD devices.

<b>Windows Server 2003:  </b>This flag is not supported.


### -field VDS_VF_DIRTY

The volume's dirty bit is set.

<b>Windows Server 2003:  </b>This flag is not supported.


### -field VDS_VF_REFS_NOT_SUPPORTED


### -field VDS_VF_BACKS_BOOT_VOLUME


### -field VDS_VF_BACKED_BY_WIM_IMAGE




## -remarks



On an MBR basic disk, volume flags can be set only for the entire disk, not for individual volumes.

If the <b>VDS_VF_NO_DEFAULT_DRIVE_LETTER</b> flag is set on an MBR disk, any existing drive letters are preserved, but no new drive letters will be assigned to volumes on the disk.

This enumeration provides values for the <b>ulFlags</b> member of the 
    <a href="https://msdn.microsoft.com/3628b312-f830-4a1c-beb7-ad002a94313c">VDS_VOLUME_PROP</a> structure and the <i>ulFlags</i> parameter of the <a href="https://msdn.microsoft.com/f426b089-6c5f-4ab4-aa92-127e24cb57b1">IVdsVolume::SetFlags</a> and <a href="https://msdn.microsoft.com/970dcd4a-ac06-4e2d-969c-82c5dabd0019">IVdsVolume::ClearFlags</a> methods.

The following table compares the behavior of the VDS_VF_NO_DEFAULT_DRIVE_LETTER flag on MBR basic disks, GPT basic disks, and dynamic disks.

<table>
<tr>
<th>Feature</th>
<th>MBR basic disks</th>
<th>GPT basic disks</th>
<th>MBR or GPT dynamic disks</th>
</tr>
<tr>
<td>The VDS_VF_NO_DEFAULT_DRIVE_LETTER flag is cleared by default. However, this flag can be set by calling <a href="https://msdn.microsoft.com/f426b089-6c5f-4ab4-aa92-127e24cb57b1">IVdsVolume::SetFlags</a>.</td>
<td>Yes.</td>
<td>Yes.</td>
<td>Yes.<b>Windows Server 2003:  </b>This flag is always set for dynamic disks and cannot be cleared.

</td>
</tr>
<tr>
<td>Assigning or removing a drive letter toggles the VDS_VF_NO_DEFAULT_DRIVE_LETTER flag setting.</td>
<td>No, because this flag is set or cleared for the entire disk.</td>
<td>Yes, because this flag is set or cleared for individual volumes.</td>
<td>Yes.<b>Windows Server 2003:  </b>This flag is always set for dynamic disks and cannot be cleared.

</td>
</tr>
</table>
 

To create a boot volume on a dynamic disk, you must set the <b>VDS_VF_INSTALLABLE</b> flag for the volume and then format the volume by calling the <a href="https://msdn.microsoft.com/8203ac16-99af-4962-bafc-12c0d238d062">IVdsVolumeMF::Format</a> method.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_VOLUME_FLAG</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_VOLUME_FLAG</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/970dcd4a-ac06-4e2d-969c-82c5dabd0019">IVdsVolume::ClearFlags</a>



<a href="https://msdn.microsoft.com/f426b089-6c5f-4ab4-aa92-127e24cb57b1">IVdsVolume::SetFlags</a>



<a href="https://msdn.microsoft.com/1ef5a1e6-0e41-4077-9ae8-fe266f2623cc">IVdsVolumeMF::Dismount</a>



<a href="https://msdn.microsoft.com/30ee6e39-c1e5-4173-a3dd-5644632140d1">VDS Enumerations</a>



<a href="https://msdn.microsoft.com/d14a852f-8a78-4631-a288-476701321ac2">VDS_PARTITION_INFO_MBR</a>



<a href="https://msdn.microsoft.com/2da99388-8ee6-4e6b-98dc-52f12290c4dc">VDS_SAN_POLICY</a>



<a href="https://msdn.microsoft.com/3628b312-f830-4a1c-beb7-ad002a94313c">VDS_VOLUME_PROP</a>
 

 

