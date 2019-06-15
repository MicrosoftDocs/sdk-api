---
UID: NF:cscobj.IOfflineFilesSyncErrorItemInfo.GetFileTimes
title: IOfflineFilesSyncErrorItemInfo::GetFileTimes (cscobj.h)
author: windows-sdk-content
description: Retrieves the last-write and change times for the item.
old-location: of\iofflinefilessyncerroriteminfo_getfiletimes.htm
tech.root: offlinefiles
ms.assetid: dec0ce0c-ef24-482f-9890-19864d9ff652
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetFileTimes, GetFileTimes method [Offline Files], GetFileTimes method [Offline Files],IOfflineFilesSyncErrorItemInfo interface, IOfflineFilesSyncErrorItemInfo interface [Offline Files],GetFileTimes method, IOfflineFilesSyncErrorItemInfo.GetFileTimes, IOfflineFilesSyncErrorItemInfo::GetFileTimes, cscobj/IOfflineFilesSyncErrorItemInfo::GetFileTimes, of.iofflinefilessyncerroriteminfo_getfiletimes
ms.topic: method
f1_keywords: ["cscobj/IOfflineFilesSyncErrorItemInfo.GetFileTimes"]
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
 - IOfflineFilesSyncErrorItemInfo.GetFileTimes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOfflineFilesSyncErrorItemInfo::GetFileTimes


## -description


Retrieves the last-write and change times for the item.


## -parameters




### -param pftLastWrite [out]

Receives a pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure containing the item's last-write time value.


### -param pftChange [out]

Receives a pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure containing the item's change time value.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilessyncerroriteminfo">IOfflineFilesSyncErrorItemInfo</a>
 

 

