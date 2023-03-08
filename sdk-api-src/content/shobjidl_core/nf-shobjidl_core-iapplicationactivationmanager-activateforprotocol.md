---
UID: NF:shobjidl_core.IApplicationActivationManager.ActivateForProtocol
title: IApplicationActivationManager::ActivateForProtocol (shobjidl_core.h)
description: Activates the specified Windows Store app for the protocol contract (Windows.Protocol).
helpviewer_keywords: ["ActivateForProtocol","ActivateForProtocol method [Windows Shell]","ActivateForProtocol method [Windows Shell]","IApplicationActivationManager interface","IApplicationActivationManager interface [Windows Shell]","ActivateForProtocol method","IApplicationActivationManager.ActivateForProtocol","IApplicationActivationManager::ActivateForProtocol","shell.IApplicationActivationManager_ActivateForProtocol","shobjidl_core/IApplicationActivationManager::ActivateForProtocol"]
old-location: shell\IApplicationActivationManager_ActivateForProtocol.htm
tech.root: shell
ms.assetid: A37E140A-5369-4abe-A9E9-8BD2E4492082
ms.date: 12/05/2018
ms.keywords: ActivateForProtocol, ActivateForProtocol method [Windows Shell], ActivateForProtocol method [Windows Shell],IApplicationActivationManager interface, IApplicationActivationManager interface [Windows Shell],ActivateForProtocol method, IApplicationActivationManager.ActivateForProtocol, IApplicationActivationManager::ActivateForProtocol, shell.IApplicationActivationManager_ActivateForProtocol, shobjidl_core/IApplicationActivationManager::ActivateForProtocol
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - IApplicationActivationManager::ActivateForProtocol
 - shobjidl_core/IApplicationActivationManager::ActivateForProtocol
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IApplicationActivationManager.ActivateForProtocol
---

# IApplicationActivationManager::ActivateForProtocol


## -description

Activates the specified Windows Store app for the protocol contract (Windows.Protocol).

## -parameters

### -param appUserModelId [in]

The application user model ID of the Windows Store app.

### -param itemArray [in]

A pointer to an array of a single Shell item. The first item in the array is converted into a Uri object that is passed to the app through <a href="/uwp/api/windows.applicationmodel.activation.protocolactivatedeventargs">ProtocolActivatedEventArgs</a>. Any items in the array except for the first element are ignored.

### -param processId [out]

A pointer to a value that, when this method returns successfully, receives the process ID of the app instance that fulfills this contract.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationactivationmanager">IApplicationActivationManager</a>