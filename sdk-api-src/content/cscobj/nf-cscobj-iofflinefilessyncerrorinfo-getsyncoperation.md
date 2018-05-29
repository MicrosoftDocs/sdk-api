---
UID: NF:cscobj.IOfflineFilesSyncErrorInfo.GetSyncOperation
title: IOfflineFilesSyncErrorInfo::GetSyncOperation
author: windows-sdk-content
description: Retrieves a value indicating the type of sync operation that was being performed when the error was encountered.
old-location: of\iofflinefilessyncerrorinfo_getsyncoperation.htm
old-project: OfflineFiles
ms.assetid: 21973fb8-26f9-40a0-bb9a-d9c5ff6924e7
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: GetSyncOperation, GetSyncOperation method [Offline Files], GetSyncOperation method [Offline Files],IOfflineFilesSyncErrorInfo interface, IOfflineFilesSyncErrorInfo interface [Offline Files],GetSyncOperation method, IOfflineFilesSyncErrorInfo.GetSyncOperation, IOfflineFilesSyncErrorInfo::GetSyncOperation, cscobj/IOfflineFilesSyncErrorInfo::GetSyncOperation, of.iofflinefilessyncerrorinfo_getsyncoperation
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
-	IOfflineFilesSyncErrorInfo.GetSyncOperation
product: Windows
targetos: Windows
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
---

# IOfflineFilesSyncErrorInfo::GetSyncOperation


## -description


Retrieves a value indicating the type of sync operation that was being performed when the error was encountered.


## -parameters




### -param pSyncOp [out]

Receives a value from the <a href="https://msdn.microsoft.com/d32db35c-4789-49e6-8c15-15d44eac95cf">OFFLINEFILES_SYNC_OPERATION</a> enumeration that indicates the operation type.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -see-also




<a href="https://msdn.microsoft.com/df1dd351-eb18-46e6-b778-852f551adfd1">IOfflineFilesSyncErrorInfo</a>
 

 

