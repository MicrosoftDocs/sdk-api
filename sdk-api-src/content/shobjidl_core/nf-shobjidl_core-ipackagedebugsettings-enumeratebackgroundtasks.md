---
UID: NF:shobjidl_core.IPackageDebugSettings.EnumerateBackgroundTasks
title: IPackageDebugSettings::EnumerateBackgroundTasks
author: windows-sdk-content
description: Gets the background tasks that are provided by the specified package.
old-location: shell\IPackageDebugSettings_EnumerateBackgroundTasks.htm
tech.root: shell
ms.assetid: 14a516c8-fb15-41b6-807c-b14d81148e0e
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: EnumerateBackgroundTasks, EnumerateBackgroundTasks method [Windows Shell], EnumerateBackgroundTasks method [Windows Shell],IPackageDebugSettings interface, IPackageDebugSettings interface [Windows Shell],EnumerateBackgroundTasks method, IPackageDebugSettings.EnumerateBackgroundTasks, IPackageDebugSettings::EnumerateBackgroundTasks, shell.IPackageDebugSettings_EnumerateBackgroundTasks, shobjidl_core/IPackageDebugSettings::EnumerateBackgroundTasks
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
 - IPackageDebugSettings.EnumerateBackgroundTasks
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPackageDebugSettings::EnumerateBackgroundTasks


## -description


Gets the background tasks that are provided by the specified package.


## -parameters




### -param packageFullName [in]

The package full name to query for background tasks.


### -param taskCount [out]

The count of <i>taskIds</i> and <i>taskNames</i> entries.


### -param taskIds [out]

An array of background task identifiers. You can use these identifiers in the <a href="https://msdn.microsoft.com/30ef83f0-cad1-4aee-9b70-0fe7189aff9e">ActivateBackgroundTask</a> method to activate specified tasks.


### -param taskNames [out]

An array of task names that corresponds with background <i>taskIds</i>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Both parameters <i>taskIds</i> and <i>taskNames</i> have the same ordering of tasks. If you need to know the user-readable task name associated with <i>taskId[0]</i>, refer to <i>taskNames[0]</i>.




## -see-also




<a href="https://msdn.microsoft.com/e407c4ca-0de1-4b17-bb83-5c4128952d48">IPackageDebugSettings</a>
 

 

