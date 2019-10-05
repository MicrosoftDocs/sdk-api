---
UID: NE:asyncinfo.AsyncStatus
title: AsyncStatus (asyncinfo.h)
author: windows-sdk-content
description: Represents the status for an asynchronous operation.
old-location: winrt\asyncstatus.htm
tech.root: WinRT
ms.assetid: 085BF8A1-087F-4B01-8A20-69730BA603B1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AsyncStatus, AsyncStatus enumeration [Windows Runtime], Cancelled, Completed, Created, Error, Started, asyncinfo/AsyncStatus, asyncinfo/Cancelled, asyncinfo/Completed, asyncinfo/Created, asyncinfo/Error, asyncinfo/Started, winrt.asyncstatus
ms.topic: enum
f1_keywords: 
 - "asyncinfo/AsyncStatus"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - AsyncInfo.h
api_name:
 - AsyncStatus
targetos: Windows
req.typenames: AsyncStatus
req.redist: 
ms.custom: 19H1
---

# AsyncStatus enumeration


## -description


Represents the status for an asynchronous operation.


## -enum-fields




### -field Started

The operation is in progress.


### -field Completed

The operation has completed without error.


### -field Canceled


### -field Error

The operation has completed with an error. No results are available.


#### - Cancelled

The client has initiated a cancellation of the operation.


#### - Created

The operation has not started.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/asyncinfo/nn-asyncinfo-iasyncinfo">IAsyncInfo</a>
 

 

