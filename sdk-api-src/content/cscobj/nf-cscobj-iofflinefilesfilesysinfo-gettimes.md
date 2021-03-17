---
UID: NF:cscobj.IOfflineFilesFileSysInfo.GetTimes
title: IOfflineFilesFileSysInfo::GetTimes (cscobj.h)
description: Retrieves the time values associated with an item.
helpviewer_keywords: ["GetTimes","GetTimes method [Offline Files]","GetTimes method [Offline Files]","IOfflineFilesFileSysInfo interface","IOfflineFilesFileSysInfo interface [Offline Files]","GetTimes method","IOfflineFilesFileSysInfo.GetTimes","IOfflineFilesFileSysInfo::GetTimes","cscobj/IOfflineFilesFileSysInfo::GetTimes","of.iofflinefilesfilesysinfo_gettimes"]
old-location: of\iofflinefilesfilesysinfo_gettimes.htm
tech.root: of
ms.assetid: 120b3f7c-6a92-4a03-8676-1ad4e4dc96b3
ms.date: 12/05/2018
ms.keywords: GetTimes, GetTimes method [Offline Files], GetTimes method [Offline Files],IOfflineFilesFileSysInfo interface, IOfflineFilesFileSysInfo interface [Offline Files],GetTimes method, IOfflineFilesFileSysInfo.GetTimes, IOfflineFilesFileSysInfo::GetTimes, cscobj/IOfflineFilesFileSysInfo::GetTimes, of.iofflinefilesfilesysinfo_gettimes
req.header: cscobj.h
req.include-header: 
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
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOfflineFilesFileSysInfo::GetTimes
 - cscobj/IOfflineFilesFileSysInfo::GetTimes
dev_langs:
 - c++
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
---

# IOfflineFilesFileSysInfo::GetTimes


## -description

Retrieves the time values associated with an item.

## -parameters

### -param copy [in]

An <a href="/windows/desktop/api/cscobj/ne-cscobj-offlinefiles_item_copy">OFFLINEFILES_ITEM_COPY</a> enumeration value identifying which copy (local or remote) to retrieve the time values for.

<b>Windows Vista:  </b>This value must be <b>OFFLINEFILES_ITEM_COPY_LOCAL</b>.

### -param pftCreationTime [out]

Receives a pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure containing the item's creation time.

### -param pftLastWriteTime [out]

Receives a pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure containing the item's last-write time.  This is the time the item's data was last written to.

### -param pftChangeTime [out]

Receives a pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure containing the item's last-change time.  This is the time the item's data or attributes were last changed.

### -param pftLastAccessTime [out]

Receives a pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure containing the item's last-access time.  This is the time the item was last read from or written to.

## -returns

Returns <b>S_OK</b> if successful, or an error value otherwise.

## -remarks

The time values returned directly correspond to the Win32 file time values used by the NTFS file system.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesfilesysinfo">IOfflineFilesFileSysInfo</a>