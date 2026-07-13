---
UID: NF:shobjidl_core.IPackageDebugSettings.GetPackageExecutionState
title: IPackageDebugSettings::GetPackageExecutionState (shobjidl_core.h)
description: Returns the current execution state of the specified package.
helpviewer_keywords: ["GetPackageExecutionState","GetPackageExecutionState method [Windows Shell]","GetPackageExecutionState method [Windows Shell]","IPackageDebugSettings interface","IPackageDebugSettings interface [Windows Shell]","GetPackageExecutionState method","IPackageDebugSettings.GetPackageExecutionState","IPackageDebugSettings::GetPackageExecutionState","shell.IPackageDebugSettings_GetPackageExecutionState","shobjidl_core/IPackageDebugSettings::GetPackageExecutionState"]
old-location: shell\IPackageDebugSettings_GetPackageExecutionState.htm
tech.root: shell
ms.assetid: 39560adc-9d35-48ec-8b70-2ed4b83dd1f6
ms.date: 12/05/2018
ms.keywords: GetPackageExecutionState, GetPackageExecutionState method [Windows Shell], GetPackageExecutionState method [Windows Shell],IPackageDebugSettings interface, IPackageDebugSettings interface [Windows Shell],GetPackageExecutionState method, IPackageDebugSettings.GetPackageExecutionState, IPackageDebugSettings::GetPackageExecutionState, shell.IPackageDebugSettings_GetPackageExecutionState, shobjidl_core/IPackageDebugSettings::GetPackageExecutionState
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
 - IPackageDebugSettings::GetPackageExecutionState
 - shobjidl_core/IPackageDebugSettings::GetPackageExecutionState
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
 - IPackageDebugSettings.GetPackageExecutionState
---

# IPackageDebugSettings::GetPackageExecutionState


## -description

Returns the current execution state of the specified package.

## -parameters

### -param packageFullName [in]

Type: <b>LPCWSTR</b>

The package full name.

### -param packageExecutionState [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-package_execution_state">PACKAGE_EXECUTION_STATE</a>*</b>

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Debuggers can use the <b>GetPackageExecutionState</b> to understand if the application currently is running, suspending, suspended, or terminated. The <b>GetPackageExecutionState</b> function doesn't provide the state of background tasks running in the package.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipackagedebugsettings">IPackageDebugSettings</a>