---
UID: NF:cscobj.IOfflineFilesProgress.Begin
title: IOfflineFilesProgress::Begin (cscobj.h)
description: Reports that an operation has begun.
helpviewer_keywords: ["Begin","Begin method [Offline Files]","Begin method [Offline Files]","IOfflineFilesProgress interface","IOfflineFilesProgress interface [Offline Files]","Begin method","IOfflineFilesProgress.Begin","IOfflineFilesProgress::Begin","cscobj/IOfflineFilesProgress::Begin","of.iofflinefilesprogress_begin"]
old-location: of\iofflinefilesprogress_begin.htm
tech.root: of
ms.assetid: d3fe6abf-fc0c-4bba-9c9f-5d0e77c27b43
ms.date: 12/05/2018
ms.keywords: Begin, Begin method [Offline Files], Begin method [Offline Files],IOfflineFilesProgress interface, IOfflineFilesProgress interface [Offline Files],Begin method, IOfflineFilesProgress.Begin, IOfflineFilesProgress::Begin, cscobj/IOfflineFilesProgress::Begin, of.iofflinefilesprogress_begin
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
 - IOfflineFilesProgress::Begin
 - cscobj/IOfflineFilesProgress::Begin
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
 - IOfflineFilesProgress.Begin
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

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesprogress">IOfflineFilesProgress</a>