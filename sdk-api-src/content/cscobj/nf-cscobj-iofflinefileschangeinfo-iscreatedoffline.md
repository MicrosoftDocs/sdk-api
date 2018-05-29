---
UID: NF:cscobj.IOfflineFilesChangeInfo.IsCreatedOffline
title: IOfflineFilesChangeInfo::IsCreatedOffline
author: windows-sdk-content
description: Determines whether an item was created in the Offline Files cache while working offline.
old-location: of\iofflinefileschangeinfo_iscreatedoffline.htm
old-project: OfflineFiles
ms.assetid: 2074df23-a2dd-45ea-9ef4-5619cebebe31
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: IOfflineFilesChangeInfo interface [Offline Files],IsCreatedOffline method, IOfflineFilesChangeInfo.IsCreatedOffline, IOfflineFilesChangeInfo::IsCreatedOffline, IsCreatedOffline, IsCreatedOffline method [Offline Files], IsCreatedOffline method [Offline Files],IOfflineFilesChangeInfo interface, cscobj/IOfflineFilesChangeInfo::IsCreatedOffline, of.iofflinefileschangeinfo_iscreatedoffline
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
-	IOfflineFilesChangeInfo.IsCreatedOffline
product: Windows
targetos: Windows
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
---

# IOfflineFilesChangeInfo::IsCreatedOffline


## -description


Determines whether an item was created in the Offline Files cache while working offline.


## -parameters




### -param pbCreatedOffline [out]

Receives <b>TRUE</b> if the item was created in the Offline Files cache while working offline, or <b>FALSE</b> otherwise.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -see-also




<a href="https://msdn.microsoft.com/0ece6120-bd5d-4e3d-b71f-7aa9a51a1568">IOfflineFilesChangeInfo</a>
 

 

