---
UID: NF:cscobj.IOfflineFilesChangeInfo.IsDirty
title: IOfflineFilesChangeInfo::IsDirty
author: windows-sdk-content
description: Determines whether an item in the Offline Files cache has been modified.
old-location: of\iofflinefileschangeinfo_isdirty.htm
tech.root: OfflineFiles
ms.assetid: 47b3bae2-d0fb-4e15-a03f-c9d5001e8786
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IOfflineFilesChangeInfo interface [Offline Files],IsDirty method, IOfflineFilesChangeInfo.IsDirty, IOfflineFilesChangeInfo::IsDirty, IsDirty, IsDirty method [Offline Files], IsDirty method [Offline Files],IOfflineFilesChangeInfo interface, cscobj/IOfflineFilesChangeInfo::IsDirty, of.iofflinefileschangeinfo_isdirty
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
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IOfflineFilesChangeInfo.IsDirty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- cscobj.h
: 
- IOfflineFilesChangeInfo.IsDirty
: 
---

# IOfflineFilesChangeInfo::IsDirty


## -description


Determines whether an item in the Offline Files cache has been modified.


## -parameters




### -param pbDirty [out]

Receives <b>TRUE</b> if the item has been modified in some way while working offline, or <b>FALSE</b> otherwise.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -remarks



When an item is modified offline, it is marked as "dirty." Such items must be synchronized to clear this "dirty" property on the item.  The Offline Files service automatically synchronizes items when an offline scope transitions to online.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb530504(v=VS.85).aspx">IOfflineFilesChangeInfo</a>
 

 

