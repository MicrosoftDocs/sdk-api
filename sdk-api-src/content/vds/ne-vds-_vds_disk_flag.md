---
UID: NE:vds._VDS_DISK_FLAG
title: "_VDS_DISK_FLAG"
author: windows-sdk-content
description: Defines the set of valid flags for a disk object.Note   Except for VDS_DF_READ_ONLY, these flags cannot be set by using the IVdsDisk::SetFlags method or cleared by using the IVdsDisk::ClearFlags method.
old-location: base\vds_disk_flag.htm
old-project: VDS
ms.assetid: a421a1c1-a82c-4e07-846c-10aa2082ab86
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: VDS_DF_AUDIO_CD, VDS_DF_BOOT_DISK, VDS_DF_BOOT_FROM_DISK, VDS_DF_CLUSTERED, VDS_DF_CRASHDUMP_DISK, VDS_DF_CURRENT_READ_ONLY, VDS_DF_DYNAMIC, VDS_DF_HAS_ARC_PATH, VDS_DF_HIBERNATIONFILE_DISK, VDS_DF_HOTSPARE, VDS_DF_MASKED, VDS_DF_PAGEFILE_DISK, VDS_DF_READ_ONLY, VDS_DF_RESERVE_CAPABLE, VDS_DF_STYLE_CONVERTIBLE, VDS_DF_SYSTEM_DISK, VDS_DISK_FLAG, VDS_DISK_FLAG enumeration [VDS], _VDS_DISK_FLAG, base.vds_disk_flag, vds/VDS_DF_AUDIO_CD, vds/VDS_DF_BOOT_DISK, vds/VDS_DF_BOOT_FROM_DISK, vds/VDS_DF_CLUSTERED, vds/VDS_DF_CRASHDUMP_DISK, vds/VDS_DF_CURRENT_READ_ONLY, vds/VDS_DF_DYNAMIC, vds/VDS_DF_HAS_ARC_PATH, vds/VDS_DF_HIBERNATIONFILE_DISK, vds/VDS_DF_HOTSPARE, vds/VDS_DF_MASKED, vds/VDS_DF_PAGEFILE_DISK, vds/VDS_DF_READ_ONLY, vds/VDS_DF_RESERVE_CAPABLE, vds/VDS_DF_STYLE_CONVERTIBLE, vds/VDS_DF_SYSTEM_DISK, vds/VDS_DISK_FLAG
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: VDS_DISK_FLAG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Vds.h
api_name:
-	VDS_DISK_FLAG
product: Windows
targetos: Windows
req.lib: VdmDbg.lib
req.dll: VdmDbg.dll
req.irql: 
req.product: Windows UI
---

# _VDS_DISK_FLAG enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the set of valid flags for a disk object.
<div class="alert"><b>Note</b>    Except for  <b>VDS_DF_READ_ONLY</b>, these flags  cannot be set by using the <a href="https://msdn.microsoft.com/0ede6a22-b15c-4afd-8d49-c963ea7e2052">IVdsDisk::SetFlags</a> method or cleared by using the <a href="https://msdn.microsoft.com/3ee43acd-6dcc-40de-9bb6-de7cfb605f15">IVdsDisk::ClearFlags</a> method.</div><div> </div>

## -enum-fields




### -field VDS_DF_AUDIO_CD

The media in a CDROM or DVD drive is an audio CD.


### -field VDS_DF_HOTSPARE

The disk is reserved for use only as hot spare.


### -field VDS_DF_RESERVE_CAPABLE

This flag is reserved for future use. Do not use.


### -field VDS_DF_MASKED

The disk is masked.


### -field VDS_DF_STYLE_CONVERTIBLE

The partition style on disk can be converted between MBR and GPT.


### -field VDS_DF_CLUSTERED

The disk is clustered.


### -field VDS_DF_READ_ONLY

This flag indicates that the disk's read-only attribute, which is maintained by the Windows operating system, is set. This attribute  can be set by using the <a href="https://msdn.microsoft.com/0ede6a22-b15c-4afd-8d49-c963ea7e2052">IVdsDisk::SetFlags</a> method and cleared by using the <a href="https://msdn.microsoft.com/3ee43acd-6dcc-40de-9bb6-de7cfb605f15">IVdsDisk::ClearFlags</a> method. This flag and the corresponding attribute do not necessarily reflect the actual read-only state of the disk, which is indicated by the <b>VDS_DF_CURRENT_READ_ONLY</b> flag.

<b>Windows Vista and Windows Server 2003:  </b>Not supported before Windows Vista with SP1 and Windows Server 2008.


### -field VDS_DF_SYSTEM_DISK

The disk hosts the current system volume. If the disk is dynamic and the volume is a mirror, the flag is set on the disk that holds the plex that was used as the system volume at startup.

<b>Windows Vista and Windows Server 2003:  </b>Not supported before Windows Vista with SP1 and Windows Server 2008.


### -field VDS_DF_BOOT_DISK

The disk hosts the current boot volume.

<b>Windows Vista and Windows Server 2003:  </b>Not supported before Windows Vista with SP1 and Windows Server 2008.


### -field VDS_DF_PAGEFILE_DISK

The disk contains a pagefile.

<b>Windows Vista and Windows Server 2003:  </b>Not supported before Windows Vista with SP1 and Windows Server 2008.


### -field VDS_DF_HIBERNATIONFILE_DISK

The disk contains the hibernation volume.

<b>Windows Vista and Windows Server 2003:  </b>Not supported before Windows Vista with SP1 and Windows Server 2008.


### -field VDS_DF_CRASHDUMP_DISK

The disk contains the crashdump volume.

<b>Windows Vista and Windows Server 2003:  </b>Not supported before Windows Vista with SP1 and Windows Server 2008.


### -field VDS_DF_HAS_ARC_PATH

The disk is visible to the computer at startup. For GPT, this flag is set for all disks. For MBR, it is set only for disks that are visible to the computer's BIOS firmware. (This is generally the first 12 disks that are connected to the computer and visible to the BIOS at startup.)

<b>Windows Vista and Windows Server 2003:  </b>Not supported before Windows Vista with SP1 and Windows Server 2008.


### -field VDS_DF_DYNAMIC

The disk is a dynamic disk.

<b>Windows Vista and Windows Server 2003:  </b>Not supported before Windows Vista with SP1 and Windows Server 2008.


### -field VDS_DF_BOOT_FROM_DISK

This flag is set on the hard disk from which the computer is configured to start.

On computers that use the BIOS firmware, this is the first hard disk that the firmware detects when the computer starts up (device 80H, or 81H if 80H is assigned to a USB flash device). If the user plugs a USB flash device into the computer before startup, this may cause device 80H to be assigned to the USB device and may cause 81H to be assigned the first hard disk detected by the firmware. Note that  in that case, this flag is not set on the USB flash device.

On computers that use the Extended Firmware Interface (EFI), this flag is set on the disk that contains the EFI System Partition (ESP) that was used to start the computer. Note that if none of the disks contain an ESP, or if there are multiple ESPs, this flag is not set on any of the disks.<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This flag is not supported.




### -field VDS_DF_CURRENT_READ_ONLY

This flag indicates that the disk is in a read-only state. If it is not set, the disk is read/write. Unlike the <b>VDS_DF_READ_ONLY</b> flag, which is used to change the disk's read-only attribute maintained by the Windows operating system, this flag reflects the actual disk state.  This flag  cannot be set by using the <a href="https://msdn.microsoft.com/0ede6a22-b15c-4afd-8d49-c963ea7e2052">IVdsDisk::SetFlags</a> method or cleared by using the <a href="https://msdn.microsoft.com/3ee43acd-6dcc-40de-9bb6-de7cfb605f15">IVdsDisk::ClearFlags</a> method.

The disk will be in a read-only state if its read-only attribute is set. However, a  disk can be in a read-only state even if its read-only attribute is not set, if the underlying hardware is read-only. For example, if the LUN is in read-only state, or if the disk is a virtual hard disk that resides on a volume that is read-only, the underlying hardware is read-only, and therefore the disk is in a read-only state.<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This flag is not supported.




### -field VDS_DF_REFS_NOT_SUPPORTED




## -remarks



This enumeration provides the values for the <b>ulFlags</b> member of the <a href="https://msdn.microsoft.com/c7c09f95-9489-46fd-8b03-cabdee4521cf">VDS_DISK_PROP</a> and <a href="https://msdn.microsoft.com/f51c2937-4b70-44fb-b626-1df072e2622a">VDS_DISK_PROP2</a> structures. The <b>VDS_DISK_PROP</b> structure is returned by the <a href="https://msdn.microsoft.com/d2046a26-852d-46b2-b060-98b4a2a92387">IVdsDisk::GetProperties</a> method. The <b>VDS_DISK_PROP2</b> structure is returned by the <a href="https://msdn.microsoft.com/ef88b61b-9139-4767-b54f-46122650e922">IVdsDisk3::GetProperties2</a> method.

All of the <b>VDS_DISK_FLAG</b> flag values are set by the VDS service; they cannot be set by applications. An exception is the <b>VDS_DF_READ_ONLY</b> flag, which can be set by using the <a href="https://msdn.microsoft.com/0ede6a22-b15c-4afd-8d49-c963ea7e2052">IVdsDisk::SetFlags</a> method and cleared by using the <a href="https://msdn.microsoft.com/3ee43acd-6dcc-40de-9bb6-de7cfb605f15">IVdsDisk::ClearFlags</a> method.

USB disks and CD-ROMs have the following restrictions and capabilities:

<ul>
<li>Dynamic disks are not supported on USB disks (including USB removable hard disks and USB flash drives).</li>
<li>A removable USB disk cannot be used as a boot disk.</li>
<li>You can <a href="http://go.microsoft.com/fwlink/p/?linkid=143085">create a bootable WinPE RAM disk on a USB flash drive or CD-ROM</a>.<b>Windows Server 2003:  </b>Not supported.

</li>
<li>A USB flash drive can have only one partition. The partition type can be MBR or GPT.</li>
</ul>
<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_DISK_FLAG</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_DISK_FLAG</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/ef88b61b-9139-4767-b54f-46122650e922">IVdsDisk3::GetProperties2</a>



<a href="https://msdn.microsoft.com/3ee43acd-6dcc-40de-9bb6-de7cfb605f15">IVdsDisk::ClearFlags</a>



<a href="https://msdn.microsoft.com/d2046a26-852d-46b2-b060-98b4a2a92387">IVdsDisk::GetProperties</a>



<a href="https://msdn.microsoft.com/0ede6a22-b15c-4afd-8d49-c963ea7e2052">IVdsDisk::SetFlags</a>



<a href="https://msdn.microsoft.com/c7c09f95-9489-46fd-8b03-cabdee4521cf">VDS_DISK_PROP</a>



<a href="https://msdn.microsoft.com/f51c2937-4b70-44fb-b626-1df072e2622a">VDS_DISK_PROP2</a>
 

 

