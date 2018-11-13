---
UID: NF:cscobj.IOfflineFilesSyncProgress.SyncItemBegin
title: IOfflineFilesSyncProgress::SyncItemBegin
author: windows-sdk-content
description: Reports that a synchronization operation on an item is beginning.
old-location: of\iofflinefilessyncprogress_syncitembegin.htm
tech.root: OfflineFiles
ms.assetid: c1cdbc30-bcc9-4023-a3a2-070fb9958609
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IOfflineFilesSyncProgress interface [Offline Files],SyncItemBegin method, IOfflineFilesSyncProgress.SyncItemBegin, IOfflineFilesSyncProgress::SyncItemBegin, SyncItemBegin, SyncItemBegin method [Offline Files], SyncItemBegin method [Offline Files],IOfflineFilesSyncProgress interface, cscobj/IOfflineFilesSyncProgress::SyncItemBegin, of.iofflinefilessyncprogress_syncitembegin
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
 - IOfflineFilesSyncProgress.SyncItemBegin
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOfflineFilesSyncProgress::SyncItemBegin


## -description


Reports that a synchronization operation on an item is beginning.


## -parameters




### -param pszFile [in]

Receives the fully qualified UNC path of the file or directory to be processed.


### -param pResponse [out]

Your implementation of this method should set this parameter to a value from the <a href="https://msdn.microsoft.com/en-us/library/Bb530650(v=VS.85).aspx">OFFLINEFILES_OP_RESPONSE</a> enumeration that indicates how the operation is to proceed.


## -returns



The return value is ignored.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb530637(v=VS.85).aspx">IOfflineFilesSyncProgress</a>
 

 

