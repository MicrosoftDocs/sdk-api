---
UID: NS:vds._VDS_VOLUME_PROP2
title: "_VDS_VOLUME_PROP2"
author: windows-sdk-content
description: Defines the properties of a volume object. This structure is identical to the VDS_VOLUME_PROP structure, except that it also includes the volume GUIDs.
old-location: base\vds_volume_prop2.htm
old-project: VDS
ms.assetid: e99aaead-f5ad-4181-9208-9158e9fac38f
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "*PVDS_VOLUME_PROP2, PVDS_VOLUME_PROP2, PVDS_VOLUME_PROP2 structure pointer, VDS_VOLUME_PROP2, VDS_VOLUME_PROP2 structure, _VDS_VOLUME_PROP2, base.vds_volume_prop2, vds/PVDS_VOLUME_PROP2, vds/VDS_VOLUME_PROP2"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: VDS_VOLUME_PROP2, *PVDS_VOLUME_PROP2
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vds.h
api_name:
 - VDS_VOLUME_PROP2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _VDS_VOLUME_PROP2 structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the properties of a <a href="https://msdn.microsoft.com/92013015-b0f5-4b92-937b-c2637f65810c">volume object</a>. This structure is identical to the <a href="https://msdn.microsoft.com/3628b312-f830-4a1c-beb7-ad002a94313c">VDS_VOLUME_PROP</a> structure, except that it also includes the volume GUIDs.


## -struct-fields




### -field id

The GUID of the volume.


### -field type

A <a href="https://msdn.microsoft.com/07a44bbf-0726-4094-9b5f-2d26b0030796">VDS_VOLUME_TYPE</a> enumeration value that specifies the volume type. Volume types are simple, spanned, striped (RAID-0), mirrored, or striped with parity (RAID-5).


### -field status

A <a href="https://msdn.microsoft.com/16159d33-08e0-47a4-a4b6-06e5f2916ea8">VDS_VOLUME_STATUS</a> enumeration value that specifies the status of the volume.


### -field health

A  <a href="https://msdn.microsoft.com/c65d9266-d691-4711-8225-a442e90d8ba3">VDS_HEALTH</a> enumeration value that specifies the health state of the volume.  


### -field TransitionState

A  <a href="https://msdn.microsoft.com/ef688d1f-136b-4bc8-8209-e30033e752e9">VDS_TRANSITION_STATE</a> enumeration value that specifies the transition state of the volume.


### -field ullSize

The size of the volume, in bytes.


### -field ulFlags

A bitmask of <a href="https://msdn.microsoft.com/3a59cc61-1efe-4027-9aca-a785a5cfaef5">VDS_VOLUME_FLAG</a> enumeration values that describe the volume.


### -field RecommendedFileSystemType

A <a href="https://msdn.microsoft.com/56f2d969-eb1c-44c2-8a12-077a02ae40dc">VDS_FILE_SYSTEM_TYPE</a> enumeration value that specifies the preferred file system for the volume. Must be one of the following: VDS_FST_NTFS, VDS_FST_FAT, VDS_FST_FAT32, VDS_FST_UDF, VDS_FST_CDFS, or VDS_FST_UNKNOWN.


### -field cbUniqueId

The length of the byte array that the <b>pUniqueId</b> member points to.


### -field pwszName

The name that was used to open a handle for the volume with the <a href="base.createfile">CreateFile</a> function. For example, \\?\GLOBALROOT\Device\HarddiskVolume1.


### -field pUniqueId

A byte array that contains the unique identifier for the volume.


## -remarks



The <a href="https://msdn.microsoft.com/9580ceb2-6b2f-4313-a140-f6fa6a366960">IVdsVolume2::GetProperties2</a>
        method returns this structure to report the properties of a <a href="https://msdn.microsoft.com/92013015-b0f5-4b92-937b-c2637f65810c">volume object</a>.

When a volume is offline, the <b>VDS_VF_PERMANENTLY_DISMOUNTED</b> flag is set in the <b>ulFlags</b> member of the <b>VDS_VOLUME_PROP2</b> structure, and the <b>VDS_VS_OFFLINE</b> volume status value is also set in the <b>status</b> member of this structure.

For GPT and dynamic volumes, the unique identifier that the <b>pUniqueId</b> member points to is globally unique.

For removable media drives, the volume exists and has its own unique identifier even if there is no media in the device. If a volume is formatted on removable media, that volume has its own unique identifier. For more information, see <a href="http://go.microsoft.com/fwlink/p/?linkid=147709">Supporting Mount Manager Requests in a Storage Class Driver</a>.

The format of the unique identifier may vary among different types of devices and volumes. For basic volumes on MBR disks, the unique identifier is based on the disk signature and partition offset. Because the disk signature and partition offset are DWORD values, the unique identifier cannot be guaranteed to be globally unique across computers.

If the disk signature changes, the volume's unique identifier also changes. Disk signature changes usually occur as a result of a collision during disk cloning.

Note that a unique identifier is not the same as a volume GUID path. To find the volume GUID paths for a volume, use the <a href="https://msdn.microsoft.com/08311403-23a9-4191-9720-3cec805de825">IVdsVolumeMF3::QueryVolumeGuidPathnames</a> method.




## -see-also




<a href="https://msdn.microsoft.com/9580ceb2-6b2f-4313-a140-f6fa6a366960">IVdsVolume2::GetProperties2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff562264">MOUNTDEV_UNIQUE_ID</a>



<a href="https://msdn.microsoft.com/6a13f5eb-0fa1-48e2-a112-b2254ca28423">VDS Structures</a>



<a href="https://msdn.microsoft.com/56f2d969-eb1c-44c2-8a12-077a02ae40dc">VDS_FILE_SYSTEM_TYPE</a>



<a href="https://msdn.microsoft.com/c65d9266-d691-4711-8225-a442e90d8ba3">VDS_HEALTH</a>



<a href="https://msdn.microsoft.com/ef688d1f-136b-4bc8-8209-e30033e752e9">VDS_TRANSITION_STATE</a>



<a href="https://msdn.microsoft.com/3a59cc61-1efe-4027-9aca-a785a5cfaef5">VDS_VOLUME_FLAG</a>



<a href="https://msdn.microsoft.com/16159d33-08e0-47a4-a4b6-06e5f2916ea8">VDS_VOLUME_STATUS</a>



<a href="https://msdn.microsoft.com/07a44bbf-0726-4094-9b5f-2d26b0030796">VDS_VOLUME_TYPE</a>
 

 

