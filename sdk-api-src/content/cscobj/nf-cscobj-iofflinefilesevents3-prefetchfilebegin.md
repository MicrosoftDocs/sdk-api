---
UID: NF:cscobj.IOfflineFilesEvents3.PrefetchFileBegin
title: IOfflineFilesEvents3::PrefetchFileBegin (cscobj.h)
description: Reports that a file prefetch operation has begun.
helpviewer_keywords: ["IOfflineFilesEvents3 interface [Offline Files]","PrefetchFileBegin method","IOfflineFilesEvents3.PrefetchFileBegin","IOfflineFilesEvents3::PrefetchFileBegin","PrefetchFileBegin","PrefetchFileBegin method [Offline Files]","PrefetchFileBegin method [Offline Files]","IOfflineFilesEvents3 interface","cscobj/IOfflineFilesEvents3::PrefetchFileBegin","of.iofflinefilesevents3_prefetchfilebegin"]
old-location: of\iofflinefilesevents3_prefetchfilebegin.htm
tech.root: of
ms.assetid: b65354ed-dc4b-491c-9672-2f5fa91093bd
ms.date: 12/05/2018
ms.keywords: IOfflineFilesEvents3 interface [Offline Files],PrefetchFileBegin method, IOfflineFilesEvents3.PrefetchFileBegin, IOfflineFilesEvents3::PrefetchFileBegin, PrefetchFileBegin, PrefetchFileBegin method [Offline Files], PrefetchFileBegin method [Offline Files],IOfflineFilesEvents3 interface, cscobj/IOfflineFilesEvents3::PrefetchFileBegin, of.iofflinefilesevents3_prefetchfilebegin
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
 - IOfflineFilesEvents3::PrefetchFileBegin
 - cscobj/IOfflineFilesEvents3::PrefetchFileBegin
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
 - IOfflineFilesEvents3.PrefetchFileBegin
---

# IOfflineFilesEvents3::PrefetchFileBegin


## -description

Reports that a file prefetch operation has begun.

## -parameters

### -param pszPath [in]

The UNC path of the file.

## -returns

Returns <b>S_OK</b> if successful, or an error value otherwise.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesevents3">IOfflineFilesEvents3</a>