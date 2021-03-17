---
UID: NF:upnp.IUPnPAsyncResult.AsyncOperationComplete
title: IUPnPAsyncResult::AsyncOperationComplete (upnp.h)
description: AsyncOperationComplete callback method provides notification of the completion of an asynchronous I/O operation.
helpviewer_keywords: ["AsyncOperationComplete","AsyncOperationComplete method [UPnP APIs]","AsyncOperationComplete method [UPnP APIs]","IUPnPAsyncResult interface","IUPnPAsyncResult interface [UPnP APIs]","AsyncOperationComplete method","IUPnPAsyncResult.AsyncOperationComplete","IUPnPAsyncResult::AsyncOperationComplete","upnp.iupnpasyncresult_asyncoperationcomplete","upnp/IUPnPAsyncResult::AsyncOperationComplete"]
old-location: upnp\iupnpasyncresult_asyncoperationcomplete.htm
tech.root: upnp
ms.assetid: C71C0A78-C3D1-4725-99E2-542786B03C8F
ms.date: 12/05/2018
ms.keywords: AsyncOperationComplete, AsyncOperationComplete method [UPnP APIs], AsyncOperationComplete method [UPnP APIs],IUPnPAsyncResult interface, IUPnPAsyncResult interface [UPnP APIs],AsyncOperationComplete method, IUPnPAsyncResult.AsyncOperationComplete, IUPnPAsyncResult::AsyncOperationComplete, upnp.iupnpasyncresult_asyncoperationcomplete, upnp/IUPnPAsyncResult::AsyncOperationComplete
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUPnPAsyncResult::AsyncOperationComplete
 - upnp/IUPnPAsyncResult::AsyncOperationComplete
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnp.dll
api_name:
 - IUPnPAsyncResult.AsyncOperationComplete
---

# IUPnPAsyncResult::AsyncOperationComplete


## -description

The <b>AsyncOperationComplete</b> callback method provides notification of the completion of  an asynchronous I/O operation.

## -parameters

### -param ullRequestID

The handle identifier corresponding to the completed asynchronous I/O operation.

## -returns

If the method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h

## -see-also

<a href="/windows/desktop/api/upnp/nn-upnp-iupnpasyncresult">IUPnPAsyncResult</a>