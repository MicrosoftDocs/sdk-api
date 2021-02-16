---
UID: NF:cscobj.IOfflineFilesEvents3.PrefetchFileEnd
title: IOfflineFilesEvents3::PrefetchFileEnd (cscobj.h)
description: Reports that a file prefetch operation has ended.
helpviewer_keywords: ["IOfflineFilesEvents3 interface [Offline Files]","PrefetchFileEnd method","IOfflineFilesEvents3.PrefetchFileEnd","IOfflineFilesEvents3::PrefetchFileEnd","PrefetchFileEnd","PrefetchFileEnd method [Offline Files]","PrefetchFileEnd method [Offline Files]","IOfflineFilesEvents3 interface","cscobj/IOfflineFilesEvents3::PrefetchFileEnd","of.iofflinefilesevents3_prefetchfileend"]
old-location: of\iofflinefilesevents3_prefetchfileend.htm
tech.root: of
ms.assetid: d5370d39-dd66-49c1-8774-cf335aa88e96
ms.date: 12/05/2018
ms.keywords: IOfflineFilesEvents3 interface [Offline Files],PrefetchFileEnd method, IOfflineFilesEvents3.PrefetchFileEnd, IOfflineFilesEvents3::PrefetchFileEnd, PrefetchFileEnd, PrefetchFileEnd method [Offline Files], PrefetchFileEnd method [Offline Files],IOfflineFilesEvents3 interface, cscobj/IOfflineFilesEvents3::PrefetchFileEnd, of.iofflinefilesevents3_prefetchfileend
req.header: cscobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOfflineFilesEvents3::PrefetchFileEnd
 - cscobj/IOfflineFilesEvents3::PrefetchFileEnd
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IOfflineFilesEvents3.PrefetchFileEnd
---

# IOfflineFilesEvents3::PrefetchFileEnd


## -description

Reports that a file prefetch operation has ended.

## -parameters

### -param pszPath [in]

The UNC path of the file.

### -param hrResult [in]

Receives the result of the operation. Contains <b>S_OK</b> if the operation completed successfully or an error value otherwise.

## -returns

Returns <b>S_OK</b> if successful, or an error value otherwise.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesevents3">IOfflineFilesEvents3</a>