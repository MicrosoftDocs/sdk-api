---
UID: NS:vdssys._STORAGE_DEPENDENCY_INFO_TYPE_2
title: "_STORAGE_DEPENDENCY_INFO_TYPE_2"
author: windows-sdk-content
description: Contains VHD or ISO storage dependency information for type 2.
old-location: vhd\storage_dependency_info_type_2.htm
old-project: VStor
ms.assetid: f3e57773-0008-4715-9136-a9b990beea58
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PSTORAGE_DEPENDENCY_INFO_TYPE_2, PSTORAGE_DEPENDENCY_INFO_TYPE_2, PSTORAGE_DEPENDENCY_INFO_TYPE_2 structure pointer [VHD], STORAGE_DEPENDENCY_INFO_TYPE_2, STORAGE_DEPENDENCY_INFO_TYPE_2 structure [VHD], _STORAGE_DEPENDENCY_INFO_TYPE_2, vdssys/PSTORAGE_DEPENDENCY_INFO_TYPE_2, vdssys/STORAGE_DEPENDENCY_INFO_TYPE_2, vhd.storage_dependency_info_type_2, virtdisk/PSTORAGE_DEPENDENCY_INFO_TYPE_2, virtdisk/STORAGE_DEPENDENCY_INFO_TYPE_2"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: vdssys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
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
req.typenames: STORAGE_DEPENDENCY_INFO_TYPE_2, *PSTORAGE_DEPENDENCY_INFO_TYPE_2
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - VirtDisk.h
 - vdssys.h
api_name:
 - STORAGE_DEPENDENCY_INFO_TYPE_2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _STORAGE_DEPENDENCY_INFO_TYPE_2 structure


## -description


Contains VHD or ISO storage dependency information for type 2.


## -struct-fields




### -field DependencyTypeFlags

A <a href="https://msdn.microsoft.com/f22bcf17-59fd-4a05-9516-2e14f173ed33">DEPENDENT_DISK_FLAG</a> enumeration.


### -field ProviderSpecificFlags

Flags specific to the VHD provider.


### -field VirtualStorageType

A <a href="https://msdn.microsoft.com/9f0c1848-fa8e-4747-a3b1-71a274695280">VIRTUAL_STORAGE_TYPE</a> structure.


### -field AncestorLevel

The ancestor level.


### -field DependencyDeviceName

The device name of the dependent device. If the device is a virtual hard drive then this will be in the 
      form \\.\PhysicalDrive<i>N</i>. If the device is a virtual CD or DVD drive 
      (ISO) then this will be in the form \\.\CDRom<i>N</i>. In either case 
      <i>N</i> is an integer that represents a unique identifier for the caller's host 
      system.


### -field HostVolumeName

The host disk volume name in the form \\?\Volume{<i>GUID</i>}\ where 
      <i>GUID</i> is the <b>GUID</b> that identifies the volume.


### -field DependentVolumeName

The name of the dependent volume, if any, in the form 
      \\?\Volume{<i>GUID</i>}\ where <i>GUID</i> is the 
      <b>GUID</b> that identifies the volume.


### -field DependentVolumeRelativePath

The relative path to the dependent volume.


## -see-also




<a href="https://msdn.microsoft.com/c9531c07-ad55-42b6-8685-7f55a47e8485">About VHD</a>



<a href="https://msdn.microsoft.com/3b5d0da0-2b23-4b7c-b007-ed3fe030926c">VHD Reference</a>
 

 

