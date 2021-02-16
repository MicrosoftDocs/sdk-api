---
UID: NF:cscobj.IOfflineFilesProgress.QueryAbort
title: IOfflineFilesProgress::QueryAbort (cscobj.h)
description: May be called during lengthy operations to determine if the operation should be canceled.
helpviewer_keywords: ["IOfflineFilesProgress interface [Offline Files]","QueryAbort method","IOfflineFilesProgress.QueryAbort","IOfflineFilesProgress::QueryAbort","QueryAbort","QueryAbort method [Offline Files]","QueryAbort method [Offline Files]","IOfflineFilesProgress interface","cscobj/IOfflineFilesProgress::QueryAbort","of.iofflinefilesprogress_queryabort"]
old-location: of\iofflinefilesprogress_queryabort.htm
tech.root: of
ms.assetid: 24b95898-0fe6-420b-83f2-ac77f493aeab
ms.date: 12/05/2018
ms.keywords: IOfflineFilesProgress interface [Offline Files],QueryAbort method, IOfflineFilesProgress.QueryAbort, IOfflineFilesProgress::QueryAbort, QueryAbort, QueryAbort method [Offline Files], QueryAbort method [Offline Files],IOfflineFilesProgress interface, cscobj/IOfflineFilesProgress::QueryAbort, of.iofflinefilesprogress_queryabort
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOfflineFilesProgress::QueryAbort
 - cscobj/IOfflineFilesProgress::QueryAbort
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
 - IOfflineFilesProgress.QueryAbort
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

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesprogress">IOfflineFilesProgress</a>