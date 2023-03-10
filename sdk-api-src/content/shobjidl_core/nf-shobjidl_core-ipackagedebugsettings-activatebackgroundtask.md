---
UID: NF:shobjidl_core.IPackageDebugSettings.ActivateBackgroundTask
title: IPackageDebugSettings::ActivateBackgroundTask (shobjidl_core.h)
description: Activates the specified background task.
helpviewer_keywords: ["ActivateBackgroundTask","ActivateBackgroundTask method [Windows Shell]","ActivateBackgroundTask method [Windows Shell]","IPackageDebugSettings interface","IPackageDebugSettings interface [Windows Shell]","ActivateBackgroundTask method","IPackageDebugSettings.ActivateBackgroundTask","IPackageDebugSettings::ActivateBackgroundTask","shell.IPackageDebugSettings_ActivateBackgroundTask","shobjidl_core/IPackageDebugSettings::ActivateBackgroundTask"]
old-location: shell\IPackageDebugSettings_ActivateBackgroundTask.htm
tech.root: shell
ms.assetid: 30ef83f0-cad1-4aee-9b70-0fe7189aff9e
ms.date: 12/05/2018
ms.keywords: ActivateBackgroundTask, ActivateBackgroundTask method [Windows Shell], ActivateBackgroundTask method [Windows Shell],IPackageDebugSettings interface, IPackageDebugSettings interface [Windows Shell],ActivateBackgroundTask method, IPackageDebugSettings.ActivateBackgroundTask, IPackageDebugSettings::ActivateBackgroundTask, shell.IPackageDebugSettings_ActivateBackgroundTask, shobjidl_core/IPackageDebugSettings::ActivateBackgroundTask
req.header: shobjidl_core.h
req.include-header: 
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
 - IPackageDebugSettings::ActivateBackgroundTask
 - shobjidl_core/IPackageDebugSettings::ActivateBackgroundTask
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl_core.h
api_name:
 - IPackageDebugSettings.ActivateBackgroundTask
---

# IPackageDebugSettings::ActivateBackgroundTask


## -description

Activates the specified background task.

## -parameters

### -param taskId [in]

The identifier of the background task to activate.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Use the <b>ActivateBackgroundTask</b> method to test the code that handles your  background tasks.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipackagedebugsettings">IPackageDebugSettings</a>