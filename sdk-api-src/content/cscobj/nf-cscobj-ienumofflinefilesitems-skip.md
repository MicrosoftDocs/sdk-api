---
UID: NF:cscobj.IEnumOfflineFilesItems.Skip
title: IEnumOfflineFilesItems::Skip
author: windows-driver-content
description: Skips over the next specified number of elements in the enumeration.
old-location: of\ienumofflinefilesitems_skip.htm
old-project: OfflineFiles
ms.assetid: e1f201c4-6ca8-49ca-af05-003a09ec86bd
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IEnumOfflineFilesItems interface [Offline Files],Skip method, IEnumOfflineFilesItems.Skip, IEnumOfflineFilesItems::Skip, Skip, Skip method [Offline Files], Skip method [Offline Files],IEnumOfflineFilesItems interface, cscobj/IEnumOfflineFilesItems::Skip, of.ienumofflinefilesitems_skip
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
-	IEnumOfflineFilesItems.Skip
product: Windows
targetos: Windows
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
---

# IEnumOfflineFilesItems::Skip


## -description


Skips over the next specified number of elements in the enumeration.


## -parameters




### -param celt [in]

Number of elements to be skipped.


## -returns



Returns <b>S_OK</b> if the number of elements skipped is <i>celt</i>; S_FALSE if a number less than <i>celt</i> is skipped; or an error value otherwise.




## -see-also




<a href="https://msdn.microsoft.com/9bb1fa14-74d2-4c6f-b8ba-47c6e78d7a4f">IEnumOfflineFilesItems</a>
 

 

