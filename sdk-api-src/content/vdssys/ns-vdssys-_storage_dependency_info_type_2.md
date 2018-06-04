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
 

 

