---
UID: NF:cscobj.IOfflineFilesSimpleProgress.ItemResult
title: IOfflineFilesSimpleProgress::ItemResult method
author: windows-driver-content
description: Reports that an item has been processed during the operation.
old-location: of\iofflinefilessimpleprogress_itemresult.htm
old-project: OfflineFiles
ms.assetid: 60ed3b12-b56e-4a58-8e37-a4a745ddb783
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IOfflineFilesSimpleProgress, IOfflineFilesSimpleProgress interface [Offline Files], ItemResult method, IOfflineFilesSimpleProgress::ItemResult, ItemResult method [Offline Files], ItemResult method [Offline Files], IOfflineFilesSimpleProgress interface, ItemResult,IOfflineFilesSimpleProgress.ItemResult, cscobj/IOfflineFilesSimpleProgress::ItemResult, of.iofflinefilessimpleprogress_itemresult
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
-	IOfflineFilesSimpleProgress.ItemResult
product: Windows
targetos: Windows
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
---

# IOfflineFilesSimpleProgress::ItemResult method


## -description



    Reports that an item has been processed during the operation.  This method is called even if the operation was unsuccessful.  Check the value received in the <i>hrResult</i> parameter to determine whether the operation was successful.


## -parameters




### -param pszFile [in]

Receives the fully qualified UNC path of the item that was processed.


### -param hrResult [in]

Receives the result of the operation for the item.  Contains S_OK if the operation completed successfully or an error value otherwise.


### -param pResponse [out]

Set this parameter to a value from the <a href="https://msdn.microsoft.com/a4b16256-7f6a-4e26-8cf2-3ef7c59ac3af">OFFLINEFILES_OP_RESPONSE</a> enumeration that indicates how the operation is to proceed.


## -returns



The return value is ignored.




## -see-also




<a href="https://msdn.microsoft.com/490f0958-125b-4c09-8ca4-07532ed8d4d4">IOfflineFilesSimpleProgress</a>
 

 

