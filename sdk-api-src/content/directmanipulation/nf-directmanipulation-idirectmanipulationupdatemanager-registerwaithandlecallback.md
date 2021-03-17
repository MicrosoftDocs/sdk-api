---
UID: NF:directmanipulation.IDirectManipulationUpdateManager.RegisterWaitHandleCallback
title: IDirectManipulationUpdateManager::RegisterWaitHandleCallback (directmanipulation.h)
description: Registers a callback that is triggered by a handle.
helpviewer_keywords: ["IDirectManipulationUpdateManager interface [Direct Manipulation]","RegisterWaitHandleCallback method","IDirectManipulationUpdateManager.RegisterWaitHandleCallback","IDirectManipulationUpdateManager::RegisterWaitHandleCallback","RegisterWaitHandleCallback","RegisterWaitHandleCallback method [Direct Manipulation]","RegisterWaitHandleCallback method [Direct Manipulation]","IDirectManipulationUpdateManager interface","directmanipulation.idirectmanipulationupdatemanager_registerwaithandlecallback","directmanipulation/IDirectManipulationUpdateManager::RegisterWaitHandleCallback"]
old-location: directmanipulation\idirectmanipulationupdatemanager_registerwaithandlecallback.htm
tech.root: directmanipulation
ms.assetid: bc0e22b8-ec27-478f-9c4b-ca192d8d52d0
ms.date: 12/05/2018
ms.keywords: IDirectManipulationUpdateManager interface [Direct Manipulation],RegisterWaitHandleCallback method, IDirectManipulationUpdateManager.RegisterWaitHandleCallback, IDirectManipulationUpdateManager::RegisterWaitHandleCallback, RegisterWaitHandleCallback, RegisterWaitHandleCallback method [Direct Manipulation], RegisterWaitHandleCallback method [Direct Manipulation],IDirectManipulationUpdateManager interface, directmanipulation.idirectmanipulationupdatemanager_registerwaithandlecallback, directmanipulation/IDirectManipulationUpdateManager::RegisterWaitHandleCallback
req.header: directmanipulation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DirectManipulation.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectManipulationUpdateManager::RegisterWaitHandleCallback
 - directmanipulation/IDirectManipulationUpdateManager::RegisterWaitHandleCallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectManipulation.h
api_name:
 - IDirectManipulationUpdateManager.RegisterWaitHandleCallback
---

# IDirectManipulationUpdateManager::RegisterWaitHandleCallback


## -description

Registers a callback that is triggered by a handle.

## -parameters

### -param handle [in]

The event handle that triggers the callback.

### -param eventHandler [in]

The event handler to call when the event is fired.

### -param cookie [out]

The unique ID of the event callback instance.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationupdatemanager">IDirectManipulationUpdateManager</a>