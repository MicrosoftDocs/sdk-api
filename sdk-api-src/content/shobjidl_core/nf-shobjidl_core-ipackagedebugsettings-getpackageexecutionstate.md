---
UID: NF:shobjidl_core.IPackageDebugSettings.GetPackageExecutionState
title: IPackageDebugSettings::GetPackageExecutionState (shobjidl_core.h)
author: windows-sdk-content
description: Returns the current execution state of the specified package.
old-location: shell\IPackageDebugSettings_GetPackageExecutionState.htm
tech.root: shell
ms.assetid: 39560adc-9d35-48ec-8b70-2ed4b83dd1f6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetPackageExecutionState, GetPackageExecutionState method [Windows Shell], GetPackageExecutionState method [Windows Shell],IPackageDebugSettings interface, IPackageDebugSettings interface [Windows Shell],GetPackageExecutionState method, IPackageDebugSettings.GetPackageExecutionState, IPackageDebugSettings::GetPackageExecutionState, shell.IPackageDebugSettings_GetPackageExecutionState, shobjidl_core/IPackageDebugSettings::GetPackageExecutionState
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl_core.h
api_name:
 - IPackageDebugSettings.GetPackageExecutionState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPackageDebugSettings::GetPackageExecutionState


## -description


Returns the current execution state of the specified package.


## -parameters




### -param packageFullName [in]

Type: <b>LPCWSTR</b>

The package full name.


### -param packageExecutionState [out]

Type: <b><a href="https://msdn.microsoft.com/8BE433AC-34E6-42D7-9F8B-63AECAC96996">PACKAGE_EXECUTION_STATE</a>*</b>


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Debuggers can use the <b>GetPackageExecutionState</b> to understand if the application currently is running, suspending, suspended, or terminated. The <b>GetPackageExecutionState</b> function doesn't provide the state of background tasks running in the package.




## -see-also




<a href="https://msdn.microsoft.com/e407c4ca-0de1-4b17-bb83-5c4128952d48">IPackageDebugSettings</a>
 

 

