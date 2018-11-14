---
UID: NF:shobjidl_core.IPackageDebugSettings.ActivateBackgroundTask
title: IPackageDebugSettings::ActivateBackgroundTask
author: windows-sdk-content
description: Activates the specified background task.
old-location: shell\IPackageDebugSettings_ActivateBackgroundTask.htm
tech.root: shell
ms.assetid: 30ef83f0-cad1-4aee-9b70-0fe7189aff9e
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ActivateBackgroundTask, ActivateBackgroundTask method [Windows Shell], ActivateBackgroundTask method [Windows Shell],IPackageDebugSettings interface, IPackageDebugSettings interface [Windows Shell],ActivateBackgroundTask method, IPackageDebugSettings.ActivateBackgroundTask, IPackageDebugSettings::ActivateBackgroundTask, shell.IPackageDebugSettings_ActivateBackgroundTask, shobjidl_core/IPackageDebugSettings::ActivateBackgroundTask
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IPackageDebugSettings.ActivateBackgroundTask
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- shobjidl_core.h
: 
- IPackageDebugSettings.ActivateBackgroundTask
: 
---

# IPackageDebugSettings::ActivateBackgroundTask


## -description


Activates the specified background task. 


## -parameters




### -param taskId [in]

The identifier of the background task to activate.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Use the <b>ActivateBackgroundTask</b> method to test the code that handles your  background tasks.




## -see-also




<a href="https://msdn.microsoft.com/e407c4ca-0de1-4b17-bb83-5c4128952d48">IPackageDebugSettings</a>
 

 

