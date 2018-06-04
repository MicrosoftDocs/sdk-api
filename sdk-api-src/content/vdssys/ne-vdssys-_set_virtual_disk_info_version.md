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

# _SET_VIRTUAL_DISK_INFO_VERSION enumeration


## -description


Contains the version of the virtual disk 
    <a href="https://msdn.microsoft.com/04b2bb75-7905-469a-abf1-15591dc64686">SET_VIRTUAL_DISK_INFO</a> structure to use in calls to 
    VHD functions. Use the different versions of the structure to set different kinds of information for the VHD.


## -enum-fields




### -field SET_VIRTUAL_DISK_INFO_UNSPECIFIED

Not used. Will fail the operation.


### -field SET_VIRTUAL_DISK_INFO_PARENT_PATH

Parent information is being set.


### -field SET_VIRTUAL_DISK_INFO_IDENTIFIER

A unique identifier is being set.

<div class="alert"><b>Note</b>  If the VHD's unique identifier changes as a result of the 
       <b>SET_VIRTUAL_DISK_INFO_IDENTIFIER</b> operation, it will break any existing differencing 
       chains on the VHD.</div>
<div> </div>

### -field SET_VIRTUAL_DISK_INFO_PARENT_PATH_WITH_DEPTH

Sets the parent file path and the child depth.

<b>Windows 7 and Windows Server 2008 R2:  </b>This value is not supported before Windows 8 and Windows Server 2012.


### -field SET_VIRTUAL_DISK_INFO_PHYSICAL_SECTOR_SIZE

Sets the physical sector size reported by the VHD.

<b>Windows 7 and Windows Server 2008 R2:  </b>This value is not supported before Windows 8 and Windows Server 2012.


### -field SET_VIRTUAL_DISK_INFO_VIRTUAL_DISK_ID

The identifier that is uniquely created when a user first creates the virtual disk to attempt to uniquely identify that virtual disk. 

<b>Windows 8 and Windows Server 2012:  </b>This value is not supported before Windows 8.1 and Windows Server 2012 R2.


### -field SET_VIRTUAL_DISK_INFO_CHANGE_TRACKING_STATE

Whether resilient change tracking (RCT) is turned on for the virtual disk.

<b>Windows 8.1 and Windows Server 2012 R2:  </b>This value is not supported before Windows 10 and Windows Server 2016.


### -field SET_VIRTUAL_DISK_INFO_PARENT_LOCATOR

The parent linkage information that differencing VHDs store. Parent linkage information is metadata used to locate and correctly identify the next parent in the virtual disk  chain. 

<b>Windows 8.1 and Windows Server 2012 R2:  </b>This value is not supported before Windows 10 and Windows Server 2016.


## -see-also




<a href="https://msdn.microsoft.com/c9531c07-ad55-42b6-8685-7f55a47e8485">About VHD</a>



<a href="https://msdn.microsoft.com/3b5d0da0-2b23-4b7c-b007-ed3fe030926c">VHD Reference</a>
 

 

