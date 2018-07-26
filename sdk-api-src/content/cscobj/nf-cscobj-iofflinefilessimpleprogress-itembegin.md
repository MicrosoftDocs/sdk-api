---
UID: NF:cscobj.IOfflineFilesSimpleProgress.ItemBegin
title: IOfflineFilesSimpleProgress::ItemBegin
author: windows-sdk-content
description: Reports that an operation on an item is beginning.
old-location: of\iofflinefilessimpleprogress_itembegin.htm
old-project: offlinefiles
ms.assetid: 0e3496ee-e987-4c37-93ff-bc8409acabde
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: IOfflineFilesSimpleProgress interface [Offline Files],ItemBegin method, IOfflineFilesSimpleProgress.ItemBegin, IOfflineFilesSimpleProgress::ItemBegin, ItemBegin, ItemBegin method [Offline Files], ItemBegin method [Offline Files],IOfflineFilesSimpleProgress interface, cscobj/IOfflineFilesSimpleProgress::ItemBegin, of.iofflinefilessimpleprogress_itembegin
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
 - IOfflineFilesSimpleProgress.ItemBegin
product: Windows
targetos: Windows
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
---

# IOfflineFilesSimpleProgress::ItemBegin


## -description


Reports that an operation on an item is beginning.


## -parameters




### -param pszFile [in]

Receives the fully qualified UNC path of the file or directory that is being processed.


### -param pResponse [out]

Set this parameter to a value from the <a href="https://msdn.microsoft.com/a4b16256-7f6a-4e26-8cf2-3ef7c59ac3af">OFFLINEFILES_OP_RESPONSE</a> enumeration that indicates how the operation is to proceed


## -returns



The return value is ignored.




## -see-also




<a href="https://msdn.microsoft.com/490f0958-125b-4c09-8ca4-07532ed8d4d4">IOfflineFilesSimpleProgress</a>
 

 

