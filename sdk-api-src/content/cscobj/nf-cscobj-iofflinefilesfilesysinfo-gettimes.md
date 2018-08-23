---
UID: NF:cscobj.IOfflineFilesFileSysInfo.GetTimes
title: IOfflineFilesFileSysInfo::GetTimes
author: windows-sdk-content
description: Retrieves the time values associated with an item.
old-location: of\iofflinefilesfilesysinfo_gettimes.htm
old-project: offlinefiles
ms.assetid: 120b3f7c-6a92-4a03-8676-1ad4e4dc96b3
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetTimes, GetTimes method [Offline Files], GetTimes method [Offline Files],IOfflineFilesFileSysInfo interface, IOfflineFilesFileSysInfo interface [Offline Files],GetTimes method, IOfflineFilesFileSysInfo.GetTimes, IOfflineFilesFileSysInfo::GetTimes, cscobj/IOfflineFilesFileSysInfo::GetTimes, of.iofflinefilesfilesysinfo_gettimes
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: cscobj.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: OFFLINEFILES_SYNC_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IOfflineFilesFileSysInfo.GetTimes
product: Windows
targetos: Windows
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
---

# IOfflineFilesFileSysInfo::GetTimes


## -description


Retrieves the time values associated with an item.


## -parameters




### -param copy [in]

An <a href="https://msdn.microsoft.com/en-us/library/Bb530646(v=VS.85).aspx">OFFLINEFILES_ITEM_COPY</a> enumeration value identifying which copy (local or remote) to retrieve the time values for.

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




<a href="https://msdn.microsoft.com/en-us/library/Bb530568(v=VS.85).aspx">IOfflineFilesFileSysInfo</a>
 

 

