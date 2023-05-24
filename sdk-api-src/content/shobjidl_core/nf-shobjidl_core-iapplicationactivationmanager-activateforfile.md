---
UID: NF:shobjidl_core.IApplicationActivationManager.ActivateForFile
title: IApplicationActivationManager::ActivateForFile (shobjidl_core.h)
description: Activates the specified Windows Store app for the file contract (Windows.File).
helpviewer_keywords: ["ActivateForFile","ActivateForFile method [Windows Shell]","ActivateForFile method [Windows Shell]","IApplicationActivationManager interface","IApplicationActivationManager interface [Windows Shell]","ActivateForFile method","IApplicationActivationManager.ActivateForFile","IApplicationActivationManager::ActivateForFile","shell.IApplicationActivationManager_ActivateForFile","shobjidl_core/IApplicationActivationManager::ActivateForFile"]
old-location: shell\IApplicationActivationManager_ActivateForFile.htm
tech.root: shell
ms.assetid: E7EBB743-4847-4966-A2EA-486BBA6A4A6F
ms.date: 08/02/2022
ms.keywords: ActivateForFile, ActivateForFile method [Windows Shell], ActivateForFile method [Windows Shell],IApplicationActivationManager interface, IApplicationActivationManager interface [Windows Shell],ActivateForFile method, IApplicationActivationManager.ActivateForFile, IApplicationActivationManager::ActivateForFile, shell.IApplicationActivationManager_ActivateForFile, shobjidl_core/IApplicationActivationManager::ActivateForFile
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
 - IApplicationActivationManager::ActivateForFile
 - shobjidl_core/IApplicationActivationManager::ActivateForFile
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
 - IApplicationActivationManager.ActivateForFile
---

# IApplicationActivationManager::ActivateForFile


## -description

Activates the specified Windows Store app for the file contract (Windows.File).

## -parameters

### -param appUserModelId [in]

The application user model ID of the Windows Store app.

### -param itemArray [in]

A pointer to an array of Shell items, each representing a file. This value is converted to a <a href="/cpp/cppcx/platform-collections-vectorview-class?view=vs-2019&preserve-view=true">VectorView</a> of <a href="/uwp/api/windows.storage.istorageitem">StorageItem</a> objects that is passed to the app through <a href="/uwp/api/windows.applicationmodel.activation.fileactivatedeventargs">FileActivatedEventArgs</a>.

### -param verb [in]

The verb being applied to the file or files specified by <i>itemArray</i>.

### -param processId [out]

A pointer to a value that, when this method returns successfully, receives the process ID of the app instance that fulfills this contract.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationactivationmanager">IApplicationActivationManager</a>