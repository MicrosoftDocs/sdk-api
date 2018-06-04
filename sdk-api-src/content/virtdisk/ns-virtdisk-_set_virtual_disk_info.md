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

# _SET_VIRTUAL_DISK_INFO structure


## -description


Contains virtual hard disk (VHD) information to use when you call the <a href="https://msdn.microsoft.com/bd4bee14-6812-4a28-8c44-2b8e8d42e697">SetVirtualDiskInformation</a> function to set VHD properties.


## -struct-fields




### -field Version

A <a href="https://msdn.microsoft.com/c9dd9d64-f96b-48f0-bc85-2f81ea3e2cb5">SET_VIRTUAL_DISK_INFO_VERSION</a> 
      enumeration that specifies the version of the 
      <b>SET_VIRTUAL_DISK_INFO</b> structure being passed to or 
      from the VHD functions. This determines the type of information set.


### -field ParentFilePath

The path to the parent backing store. Set the <b>Version</b> member to 
       <b>SET_VIRTUAL_DISK_INFO_PARENT_PATH</b> (1).


### -field UniqueIdentifier

The unique identifier of the VHD. Set the <b>Version</b> member to 
       <b>SET_VIRTUAL_DISK_INFO_IDENTIFIER</b> (2).


### -field ParentPathWithDepthInfo

Sets the parent file path and the child depth. Set the <b>Version</b> member to 
        <b>SET_VIRTUAL_DISK_INFO_PARENT_PATH_WITH_DEPTH</b> (3).

<b>Windows 7 and Windows Server 2008 R2:  </b>This is not supported before Windows 8 and Windows Server 2012.


### -field ParentPathWithDepthInfo.ChildDepth

Specifies the depth to the child from the leaf. The leaf itself is at depth 1.


### -field ParentPathWithDepthInfo.ParentFilePath

Specifies the depth to the parent from the leaf. The leaf itself is at depth 1.


### -field VhdPhysicalSectorSize

Sets the physical sector size reported by the VHD. Set the <b>Version</b> member to 
        <b>SET_VIRTUAL_DISK_INFO_PHYSICAL_SECTOR_SIZE</b> (4).<b>Windows 7 and Windows Server 2008 R2:  </b>This is not supported before Windows 8 and Windows Server 2012.




### -field VirtualDiskId

The identifier that is uniquely created when a user first creates the  virtual disk to attempt to uniquely identify that virtual disk. Set the <b>Version</b> member to 
        <b>SET_VIRTUAL_DISK_INFO_VIRTUAL_DISK_ID</b> (5).

<b>Windows 8 and Windows Server 2012:  </b>This is not supported before Windows 8.1 and Windows Server 2012 R2.


### -field ChangeTrackingEnabled

Turns  resilient change tracking (RCT) on or off for the VHD. <b>TRUE</b> turns RCT on. <b>FALSE</b> turns RCT off. Set the <b>Version</b> member to 
        <b>SET_VIRTUAL_DISK_INFO_CHANGE_TRACKING_STATE</b> (6).

<b>Windows 8.1 and Windows Server 2012 R2:  </b>This member is not supported before Windows 10 and Windows Server 2016.


### -field ParentLocator

Sets the parent linkage information that differencing VHDs store. Parent linkage information is metadata used to locate and correctly identify the next parent in the virtual disk  chain. Set the <b>Version</b> member to 
        <b>SET_VIRTUAL_DISK_INFO_PARENT_LOCATOR</b> (7).

<b>Windows 8.1 and Windows Server 2012 R2:  </b>This member is not supported before Windows 10 and Windows Server 2016.


### -field ParentLocator.LinkageId

The unique identifier for the parent linkage information.


### -field ParentLocator.ParentFilePath

The path of the file for the parent VHD.


## -see-also




<a href="https://msdn.microsoft.com/c9531c07-ad55-42b6-8685-7f55a47e8485">About VHD</a>



<a href="https://msdn.microsoft.com/3b5d0da0-2b23-4b7c-b007-ed3fe030926c">VHD Reference</a>
 

 

