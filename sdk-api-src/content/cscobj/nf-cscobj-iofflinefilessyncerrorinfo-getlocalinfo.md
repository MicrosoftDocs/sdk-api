---
UID: NF:cscobj.IOfflineFilesSyncErrorInfo.GetLocalInfo
title: IOfflineFilesSyncErrorInfo::GetLocalInfo
author: windows-sdk-content
description: Retrieves an instance of the IOfflineFilesSyncErrorItemInfo interface containing the file times, size, and attributes of the local copy of the item involved in the synchronization.
old-location: of\iofflinefilessyncerrorinfo_getlocalinfo.htm
old-project: offlinefiles
ms.assetid: 53e03524-9cb6-4b91-8b2a-bf428a16140e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetLocalInfo, GetLocalInfo method [Offline Files], GetLocalInfo method [Offline Files],IOfflineFilesSyncErrorInfo interface, IOfflineFilesSyncErrorInfo interface [Offline Files],GetLocalInfo method, IOfflineFilesSyncErrorInfo.GetLocalInfo, IOfflineFilesSyncErrorInfo::GetLocalInfo, cscobj/IOfflineFilesSyncErrorInfo::GetLocalInfo, of.iofflinefilessyncerrorinfo_getlocalinfo
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
 - IOfflineFilesSyncErrorInfo.GetLocalInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
---

# IOfflineFilesSyncErrorInfo::GetLocalInfo


## -description


Retrieves an instance of the <a href="https://msdn.microsoft.com/en-us/library/Bb530633(v=VS.85).aspx">IOfflineFilesSyncErrorItemInfo</a> interface containing the file times, size, and attributes of the local copy of the item involved in the synchronization.  


## -parameters




### -param ppInfo [out]

Receives the address of an instance of <a href="https://msdn.microsoft.com/en-us/library/Bb530633(v=VS.85).aspx">IOfflineFilesSyncErrorItemInfo</a> containing information about the local item copy involved in the synchronization.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb530625(v=VS.85).aspx">IOfflineFilesSyncErrorInfo</a>
 

 

