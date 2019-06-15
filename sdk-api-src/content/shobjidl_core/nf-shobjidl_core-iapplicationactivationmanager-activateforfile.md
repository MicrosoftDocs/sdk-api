---
UID: NF:shobjidl_core.IApplicationActivationManager.ActivateForFile
title: IApplicationActivationManager::ActivateForFile (shobjidl_core.h)
author: windows-sdk-content
description: Activates the specified Windows Store app for the file contract (Windows.File).
old-location: shell\IApplicationActivationManager_ActivateForFile.htm
tech.root: shell
ms.assetid: E7EBB743-4847-4966-A2EA-486BBA6A4A6F
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ActivateForFile, ActivateForFile method [Windows Shell], ActivateForFile method [Windows Shell],IApplicationActivationManager interface, IApplicationActivationManager interface [Windows Shell],ActivateForFile method, IApplicationActivationManager.ActivateForFile, IApplicationActivationManager::ActivateForFile, shell.IApplicationActivationManager_ActivateForFile, shobjidl_core/IApplicationActivationManager::ActivateForFile
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IApplicationActivationManager.ActivateForFile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IApplicationActivationManager::ActivateForFile


## -description


Activates the specified Windows Store app for the file contract (Windows.File).


## -parameters




### -param appUserModelId [in]

The application user model ID of the Windows Store app.


### -param itemArray [in]

A pointer to an array of Shell items, each representing a file. This value is converted to a <a href="https://docs.microsoft.com/en-us/cpp/cppcx/platform-collections-vectorview-class?view=vs-2019">VectorView</a> of <a href="https://docs.microsoft.com/en-us/uwp/api/windows.storage.istorageitem">StorageItem</a> objects that is passed to the app through <a href="https://docs.microsoft.com/en-us/uwp/api/windows.applicationmodel.activation.fileactivatedeventargs">FileActivatedEventArgs</a>.


### -param verb [in]

The verb being applied to the file or files specified by <i>itemArray</i>.


### -param processId [out]

A pointer to a value that, when this method returns successfully, receives the process ID of the app instance that fulfils this contract.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationactivationmanager">IApplicationActivationManager</a>
 

 

