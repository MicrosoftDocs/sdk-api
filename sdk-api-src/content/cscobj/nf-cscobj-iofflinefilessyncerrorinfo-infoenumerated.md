---
UID: NF:cscobj.IOfflineFilesSyncErrorInfo.InfoEnumerated
title: IOfflineFilesSyncErrorInfo::InfoEnumerated
author: windows-sdk-content
description: Indicates whether information was queried for the local, remote, or original copy of the item during synchronization.
old-location: of\iofflinefilessyncerrorinfo_infoenumerated.htm
tech.root: offlinefiles
ms.assetid: d2e8ae5b-92e7-4284-a02f-6eb3ab288376
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IOfflineFilesSyncErrorInfo interface [Offline Files],InfoEnumerated method, IOfflineFilesSyncErrorInfo.InfoEnumerated, IOfflineFilesSyncErrorInfo::InfoEnumerated, InfoEnumerated, InfoEnumerated method [Offline Files], InfoEnumerated method [Offline Files],IOfflineFilesSyncErrorInfo interface, cscobj/IOfflineFilesSyncErrorInfo::InfoEnumerated, of.iofflinefilessyncerrorinfo_infoenumerated
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
 - IOfflineFilesSyncErrorInfo.InfoEnumerated
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOfflineFilesSyncErrorInfo::InfoEnumerated


## -description


Indicates whether information was queried for the local, remote, or original copy of the item during synchronization. 


## -parameters




### -param pbLocalEnumerated [out]

Receives <b>TRUE</b> if information was queried for the local copy of the item during synchronization, or <b>FALSE</b> otherwise.


### -param pbRemoteEnumerated [out]

Receives <b>TRUE</b> if information was queried for the remote copy of the item during synchronization, or <b>FALSE</b> otherwise.


### -param pbOriginalEnumerated [out]

Receives <b>TRUE</b> if information was queried for the original copy of the item during synchronization, or <b>FALSE</b> otherwise.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb530625(v=VS.85).aspx">IOfflineFilesSyncErrorInfo</a>
 

 

