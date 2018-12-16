---
UID: NF:cscobj.IOfflineFilesSyncProgress.SyncItemResult
title: IOfflineFilesSyncProgress::SyncItemResult
author: windows-sdk-content
description: Reports that an item has been processed during the synchronization operation.
old-location: of\iofflinefilessyncprogress_syncitemresult.htm
tech.root: offlinefiles
ms.assetid: 2a93d52e-6b91-4d91-9372-5f0718621841
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IOfflineFilesSyncProgress interface [Offline Files],SyncItemResult method, IOfflineFilesSyncProgress.SyncItemResult, IOfflineFilesSyncProgress::SyncItemResult, SyncItemResult, SyncItemResult method [Offline Files], SyncItemResult method [Offline Files],IOfflineFilesSyncProgress interface, cscobj/IOfflineFilesSyncProgress::SyncItemResult, of.iofflinefilessyncprogress_syncitemresult
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
 - IOfflineFilesSyncProgress.SyncItemResult
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOfflineFilesSyncProgress::SyncItemResult


## -description


Reports that an item has been processed during the synchronization operation.  This method is called even if the operation was unsuccessful.  Check the value received in the <i>hrResult</i> parameter to determine whether the operation was successful.


## -parameters




### -param pszFile [in]

Receives the fully qualified UNC path of the item that was processed.


### -param hrResult [in]

Receives the result of the operation for the item.  Contains S_OK if the operation completed successfully or an error value otherwise.


### -param pErrorInfo [in]

Receives a pointer to an instance of the <a href="https://msdn.microsoft.com/df1dd351-eb18-46e6-b778-852f551adfd1">IOfflineFilesSyncErrorInfo</a> interface that provides detailed information about the result of the sync operation.


### -param pResponse [out]

Set this parameter to a value from the <a href="https://msdn.microsoft.com/a4b16256-7f6a-4e26-8cf2-3ef7c59ac3af">OFFLINEFILES_OP_RESPONSE</a> enumeration that indicates how the operation is to proceed.


## -returns



The return value is ignored.




## -see-also




<a href="https://msdn.microsoft.com/7fc5ff29-be9d-4fad-96a8-94058bb708fa">IOfflineFilesSyncProgress</a>
 

 

