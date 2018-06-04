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

# _DEPENDENT_DISK_FLAG enumeration


## -description


Contains virtual hard disk (VHD) dependency information flags.


## -enum-fields




### -field DEPENDENT_DISK_FLAG_NONE

 No flags specified. Use system defaults.


### -field DEPENDENT_DISK_FLAG_MULT_BACKING_FILES

Multiple files backing the virtual disk.


### -field DEPENDENT_DISK_FLAG_FULLY_ALLOCATED

Fully allocated virtual disk.


### -field DEPENDENT_DISK_FLAG_READ_ONLY

Read-only virtual disk.


### -field DEPENDENT_DISK_FLAG_REMOTE

 The backing file of the virtual disk is not on a local physical disk.


### -field DEPENDENT_DISK_FLAG_SYSTEM_VOLUME

 Reserved.


### -field DEPENDENT_DISK_FLAG_SYSTEM_VOLUME_PARENT

The backing file of the virtual disk is on the system volume.


### -field DEPENDENT_DISK_FLAG_REMOVABLE

The backing file of the virtual disk is on a removable physical disk.


### -field DEPENDENT_DISK_FLAG_NO_DRIVE_LETTER

Drive letters are not automatically assigned to the volumes on the virtual disk.


### -field DEPENDENT_DISK_FLAG_PARENT

The virtual disk is a parent of a differencing chain.


### -field DEPENDENT_DISK_FLAG_NO_HOST_DISK

 The virtual disk is not attached to the local host.
    For example, it is attached to a guest <a href="http://go.microsoft.com/fwlink/p/?linkid=128149">virtual machine</a>.


### -field DEPENDENT_DISK_FLAG_PERMANENT_LIFETIME

The lifetime of the virtual disk is not tied to any application or process.


## -see-also




<a href="https://msdn.microsoft.com/c9531c07-ad55-42b6-8685-7f55a47e8485">About VHD</a>



<a href="https://msdn.microsoft.com/3b5d0da0-2b23-4b7c-b007-ed3fe030926c">VHD Reference</a>



<a href="https://msdn.microsoft.com/7d5f5d02-5aad-4d64-a3a9-ddfa5a4b01c5">Virtual Storage</a>
 

 

