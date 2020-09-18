---
UID: NE:asyncinfo.AsyncStatus
title: AsyncStatus (asyncinfo.h)
description: Represents the status for an asynchronous operation.
helpviewer_keywords: ["AsyncStatus","AsyncStatus enumeration [Windows Runtime]","Cancelled","Completed","Created","Error","Started","asyncinfo/AsyncStatus","asyncinfo/Cancelled","asyncinfo/Completed","asyncinfo/Created","asyncinfo/Error","asyncinfo/Started","winrt.asyncstatus"]
old-location: winrt\asyncstatus.htm
tech.root: WinRT
ms.assetid: 085BF8A1-087F-4B01-8A20-69730BA603B1
ms.date: 12/05/2018
ms.keywords: AsyncStatus, AsyncStatus enumeration [Windows Runtime], Cancelled, Completed, Created, Error, Started, asyncinfo/AsyncStatus, asyncinfo/Cancelled, asyncinfo/Completed, asyncinfo/Created, asyncinfo/Error, asyncinfo/Started, winrt.asyncstatus
req.header: asyncinfo.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: AsyncInfo.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: AsyncStatus
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AsyncStatus
 - asyncinfo/AsyncStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - AsyncInfo.h
api_name:
 - AsyncStatus
---

## -description

Represents the status for an asynchronous operation.

## -enum-fields

### -field Started

The operation is in progress.

### -field Completed

The operation has completed without error.

### -field Canceled

The client has initiated a cancellation of the operation.

### -field Error

The operation has completed with an error. No results are available.

## -see-also

<a href="/windows/desktop/api/asyncinfo/nn-asyncinfo-iasyncinfo">IAsyncInfo</a>