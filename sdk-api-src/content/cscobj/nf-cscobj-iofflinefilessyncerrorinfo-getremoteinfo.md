---
UID: NF:cscobj.IOfflineFilesSyncErrorInfo.GetRemoteInfo
title: IOfflineFilesSyncErrorInfo::GetRemoteInfo (cscobj.h)
author: windows-sdk-content
description: Retrieves an instance of the IOfflineFilesSyncErrorItemInfo interface containing the file times, size, and attributes of the remote copy of the item involved in the synchronization.
old-location: of\iofflinefilessyncerrorinfo_getremoteinfo.htm
tech.root: offlinefiles
ms.assetid: 8b036680-b74c-485f-adae-88e59fc5e84c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetRemoteInfo, GetRemoteInfo method [Offline Files], GetRemoteInfo method [Offline Files],IOfflineFilesSyncErrorInfo interface, IOfflineFilesSyncErrorInfo interface [Offline Files],GetRemoteInfo method, IOfflineFilesSyncErrorInfo.GetRemoteInfo, IOfflineFilesSyncErrorInfo::GetRemoteInfo, cscobj/IOfflineFilesSyncErrorInfo::GetRemoteInfo, of.iofflinefilessyncerrorinfo_getremoteinfo
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
 - IOfflineFilesSyncErrorInfo.GetRemoteInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOfflineFilesSyncErrorInfo::GetRemoteInfo


## -description


Retrieves an instance of the <a href="https://msdn.microsoft.com/0af039a6-f0dd-4117-a174-38d32cfc0220">IOfflineFilesSyncErrorItemInfo</a> interface containing the file times, size, and attributes of the remote copy of the item involved in the synchronization.  


## -parameters




### -param ppInfo [out]

Receives the address of an instance of <a href="https://msdn.microsoft.com/0af039a6-f0dd-4117-a174-38d32cfc0220">IOfflineFilesSyncErrorItemInfo</a> containing information about the remote item copy involved in the synchronization.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -see-also




<a href="https://msdn.microsoft.com/df1dd351-eb18-46e6-b778-852f551adfd1">IOfflineFilesSyncErrorInfo</a>
 

 

