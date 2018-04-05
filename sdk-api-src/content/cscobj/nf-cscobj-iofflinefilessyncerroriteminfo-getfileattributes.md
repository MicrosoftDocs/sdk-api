---
UID: NF:cscobj.IOfflineFilesSyncErrorItemInfo.GetFileAttributes
title: IOfflineFilesSyncErrorItemInfo::GetFileAttributes method
author: windows-driver-content
description: Retrieves the Win32 file attributes for the item.
old-location: of\iofflinefilessyncerroriteminfo_getfileattributes.htm
old-project: OfflineFiles
ms.assetid: 4e14d571-230b-4757-8e81-2fb8dc6b9c3f
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetFileAttributes method [Offline Files], GetFileAttributes method [Offline Files], IOfflineFilesSyncErrorItemInfo interface, GetFileAttributes,IOfflineFilesSyncErrorItemInfo.GetFileAttributes, IOfflineFilesSyncErrorItemInfo, IOfflineFilesSyncErrorItemInfo interface [Offline Files], GetFileAttributes method, IOfflineFilesSyncErrorItemInfo::GetFileAttributes, cscobj/IOfflineFilesSyncErrorItemInfo::GetFileAttributes, of.iofflinefilessyncerroriteminfo_getfileattributes
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: OFFLINEFILES_SYNC_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CscSvc.dll
-	CscObj.dll
api_name:
-	IOfflineFilesSyncErrorItemInfo.GetFileAttributes
product: Windows
targetos: Windows
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
---

# IOfflineFilesSyncErrorItemInfo::GetFileAttributes method


## -description


Retrieves the Win32 file attributes for the item.


## -parameters




### -param pdwAttributes [out]

Receives the file attribute mask for the item.  One or more of FILE_ATTRIBUTE_XXXXXX as defined in the Windows SDK. For more information, see the <a href="https://msdn.microsoft.com/9f9bcdbb-1ffd-49c2-92f4-181fdcc9c690">GetFileAttributes</a> function.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -see-also




<a href="https://msdn.microsoft.com/0af039a6-f0dd-4117-a174-38d32cfc0220">IOfflineFilesSyncErrorItemInfo</a>
 

 

