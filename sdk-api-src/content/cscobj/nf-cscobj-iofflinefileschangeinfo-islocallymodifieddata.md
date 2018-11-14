---
UID: NF:cscobj.IOfflineFilesChangeInfo.IsLocallyModifiedData
title: IOfflineFilesChangeInfo::IsLocallyModifiedData
author: windows-sdk-content
description: Determines whether an item's data was modified while working offline.
old-location: of\iofflinefileschangeinfo_islocallymodifieddata.htm
tech.root: OfflineFiles
ms.assetid: d27999af-147e-4c1b-be89-58191292337d
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IOfflineFilesChangeInfo interface [Offline Files],IsLocallyModifiedData method, IOfflineFilesChangeInfo.IsLocallyModifiedData, IOfflineFilesChangeInfo::IsLocallyModifiedData, IsLocallyModifiedData, IsLocallyModifiedData method [Offline Files], IsLocallyModifiedData method [Offline Files],IOfflineFilesChangeInfo interface, cscobj/IOfflineFilesChangeInfo::IsLocallyModifiedData, of.iofflinefileschangeinfo_islocallymodifieddata
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
 - IOfflineFilesChangeInfo.IsLocallyModifiedData
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
- IOfflineFilesChangeInfo.IsLocallyModifiedData
: 
---

# IOfflineFilesChangeInfo::IsLocallyModifiedData


## -description


Determines whether an item's data was modified while working offline.


## -parameters




### -param pbLocallyModifiedData [out]

Receives <b>TRUE</b> if the item's data was modified in the Offline Files cache while working offline, or <b>FALSE</b> otherwise.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb530504(v=VS.85).aspx">IOfflineFilesChangeInfo</a>
 

 

