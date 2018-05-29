---
UID: NF:cscobj.IOfflineFilesSyncErrorInfo.GetOriginalInfo
title: IOfflineFilesSyncErrorInfo::GetOriginalInfo
author: windows-sdk-content
description: Retrieves an instance of the IOfflineFilesSyncErrorItemInfo interface containing the file times, size, and attributes of the original copy of the item involved in the synchronization.
old-location: of\iofflinefilessyncerrorinfo_getoriginalinfo.htm
old-project: OfflineFiles
ms.assetid: 1cf3a21c-5ae1-475c-9eb7-2d520ee2ce79
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: GetOriginalInfo, GetOriginalInfo method [Offline Files], GetOriginalInfo method [Offline Files],IOfflineFilesSyncErrorInfo interface, IOfflineFilesSyncErrorInfo interface [Offline Files],GetOriginalInfo method, IOfflineFilesSyncErrorInfo.GetOriginalInfo, IOfflineFilesSyncErrorInfo::GetOriginalInfo, cscobj/IOfflineFilesSyncErrorInfo::GetOriginalInfo, of.iofflinefilessyncerrorinfo_getoriginalinfo
ms.prod: windows
ms.technology: windows-sdk
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
-	IOfflineFilesSyncErrorInfo.GetOriginalInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
---

# IOfflineFilesSyncErrorInfo::GetOriginalInfo


## -description


Retrieves an instance of the <a href="https://msdn.microsoft.com/0af039a6-f0dd-4117-a174-38d32cfc0220">IOfflineFilesSyncErrorItemInfo</a> interface containing the file times, size, and attributes of the original copy of the item involved in the synchronization.

"Original" refers to the state information recorded the last time the cached item was in sync with the server.


## -parameters




### -param ppInfo [out]

Receives the address of an instance of <a href="https://msdn.microsoft.com/0af039a6-f0dd-4117-a174-38d32cfc0220">IOfflineFilesSyncErrorItemInfo</a> containing information about the original item copy involved in the synchronization.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -see-also




<a href="https://msdn.microsoft.com/df1dd351-eb18-46e6-b778-852f551adfd1">IOfflineFilesSyncErrorInfo</a>
 

 

