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

# IOfflineFilesFileSysInfo::GetTimes


## -description


Retrieves the time values associated with an item.


## -parameters




### -param copy [in]

An <a href="https://msdn.microsoft.com/b956f186-962b-457e-9c03-ffd1a7f937ca">OFFLINEFILES_ITEM_COPY</a> enumeration value identifying which copy (local or remote) to retrieve the time values for.

<b>Windows Vista:  </b>This value must be <b>OFFLINEFILES_ITEM_COPY_LOCAL</b>.


### -param pftCreationTime [out]

Receives a pointer to a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure containing the item's creation time.


### -param pftLastWriteTime [out]

Receives a pointer to a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure containing the item's last-write time.  This is the time the item's data was last written to.


### -param pftChangeTime [out]

Receives a pointer to a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure containing the item's last-change time.  This is the time the item's data or attributes were last changed.


### -param pftLastAccessTime [out]

Receives a pointer to a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure containing the item's last-access time.  This is the time the item was last read from or written to.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -remarks



The time values returned directly correspond to the Win32 file time values used by the NTFS file system.




## -see-also




<a href="https://msdn.microsoft.com/d3da183d-eb12-4411-b461-b58689ef5bff">IOfflineFilesFileSysInfo</a>
 

 

