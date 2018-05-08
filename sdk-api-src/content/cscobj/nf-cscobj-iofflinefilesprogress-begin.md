---
UID: NF:cscobj.IOfflineFilesProgress.Begin
title: IOfflineFilesProgress::Begin
author: windows-driver-content
description: Reports that an operation has begun.
old-location: of\iofflinefilesprogress_begin.htm
old-project: OfflineFiles
ms.assetid: d3fe6abf-fc0c-4bba-9c9f-5d0e77c27b43
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: Begin, Begin method [Offline Files], Begin method [Offline Files],IOfflineFilesProgress interface, IOfflineFilesProgress interface [Offline Files],Begin method, IOfflineFilesProgress.Begin, IOfflineFilesProgress::Begin, cscobj/IOfflineFilesProgress::Begin, of.iofflinefilesprogress_begin
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
-	IOfflineFilesProgress.Begin
product: Windows
targetos: Windows
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
---

# IOfflineFilesProgress::Begin


## -description


Reports that an operation has begun.


## -parameters




### -param pbAbort [out]

Set this value to <b>TRUE</b> to cancel the operation.   Set to <b>FALSE</b> to continue.


## -returns



The return value is ignored.




## -see-also




<a href="https://msdn.microsoft.com/b568a8c6-119b-486e-94e3-fe4e54a395bb">IOfflineFilesProgress</a>
 

 

