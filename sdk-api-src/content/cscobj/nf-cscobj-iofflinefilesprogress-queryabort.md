---
UID: NF:cscobj.IOfflineFilesProgress.QueryAbort
title: IOfflineFilesProgress::QueryAbort
author: windows-driver-content
description: May be called during lengthy operations to determine if the operation should be canceled.
old-location: of\iofflinefilesprogress_queryabort.htm
old-project: OfflineFiles
ms.assetid: 24b95898-0fe6-420b-83f2-ac77f493aeab
ms.author: windowsdriverdev
ms.date: 5/11/2018
ms.keywords: IOfflineFilesProgress interface [Offline Files],QueryAbort method, IOfflineFilesProgress.QueryAbort, IOfflineFilesProgress::QueryAbort, QueryAbort, QueryAbort method [Offline Files], QueryAbort method [Offline Files],IOfflineFilesProgress interface, cscobj/IOfflineFilesProgress::QueryAbort, of.iofflinefilesprogress_queryabort
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
-	IOfflineFilesProgress.QueryAbort
product: Windows
targetos: Windows
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
---

# IOfflineFilesProgress::QueryAbort


## -description


May be called during lengthy operations to determine if the operation should be canceled.


## -parameters




### -param pbAbort [out]

Set this value to <b>TRUE</b> to cancel the operation.   Set to <b>FALSE</b> to continue.


## -returns



The return value is ignored.




## -remarks



This method may be used by the implementation in cases where calls to other progress methods are infrequent.  The sole purpose of this method is to determine if the operation should be canceled immediately.




## -see-also




<a href="https://msdn.microsoft.com/b568a8c6-119b-486e-94e3-fe4e54a395bb">IOfflineFilesProgress</a>
 

 

