---
UID: NF:upnp.IUPnPAsyncResult.AsyncOperationComplete
title: IUPnPAsyncResult::AsyncOperationComplete
author: windows-sdk-content
description: AsyncOperationComplete callback method provides notification of the completion of an asynchronous I/O operation.
old-location: upnp\iupnpasyncresult_asyncoperationcomplete.htm
tech.root: UPnP
ms.assetid: C71C0A78-C3D1-4725-99E2-542786B03C8F
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: AsyncOperationComplete, AsyncOperationComplete method [UPnP APIs], AsyncOperationComplete method [UPnP APIs],IUPnPAsyncResult interface, IUPnPAsyncResult interface [UPnP APIs],AsyncOperationComplete method, IUPnPAsyncResult.AsyncOperationComplete, IUPnPAsyncResult::AsyncOperationComplete, upnp.iupnpasyncresult_asyncoperationcomplete, upnp/IUPnPAsyncResult::AsyncOperationComplete
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: upnp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.dll: Upnp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnp.dll
api_name:
 - IUPnPAsyncResult.AsyncOperationComplete
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUPnPAsyncResult::AsyncOperationComplete


## -description


The <b>AsyncOperationComplete</b> callback method provides notification of the completion of  an asynchronous I/O operation.


## -parameters




### -param ullRequestID

TBD




#### - ullRequestId

The handle identifier corresponding to the completed asynchronous I/O operation.


## -returns



If the method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h




## -see-also




<a href="https://msdn.microsoft.com/53854510-BB0C-41E6-8651-F34991B24D5E">IUPnPAsyncResult</a>
 

 

