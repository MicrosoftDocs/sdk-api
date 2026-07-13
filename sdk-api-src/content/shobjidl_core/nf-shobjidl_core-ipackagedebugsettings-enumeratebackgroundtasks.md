---
UID: NF:shobjidl_core.IPackageDebugSettings.EnumerateBackgroundTasks
title: IPackageDebugSettings::EnumerateBackgroundTasks (shobjidl_core.h)
description: Gets the background tasks that are provided by the specified package.
helpviewer_keywords: ["EnumerateBackgroundTasks","EnumerateBackgroundTasks method [Windows Shell]","EnumerateBackgroundTasks method [Windows Shell]","IPackageDebugSettings interface","IPackageDebugSettings interface [Windows Shell]","EnumerateBackgroundTasks method","IPackageDebugSettings.EnumerateBackgroundTasks","IPackageDebugSettings::EnumerateBackgroundTasks","shell.IPackageDebugSettings_EnumerateBackgroundTasks","shobjidl_core/IPackageDebugSettings::EnumerateBackgroundTasks"]
old-location: shell\IPackageDebugSettings_EnumerateBackgroundTasks.htm
tech.root: shell
ms.assetid: 14a516c8-fb15-41b6-807c-b14d81148e0e
ms.date: 12/05/2018
ms.keywords: EnumerateBackgroundTasks, EnumerateBackgroundTasks method [Windows Shell], EnumerateBackgroundTasks method [Windows Shell],IPackageDebugSettings interface, IPackageDebugSettings interface [Windows Shell],EnumerateBackgroundTasks method, IPackageDebugSettings.EnumerateBackgroundTasks, IPackageDebugSettings::EnumerateBackgroundTasks, shell.IPackageDebugSettings_EnumerateBackgroundTasks, shobjidl_core/IPackageDebugSettings::EnumerateBackgroundTasks
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
 - IPackageDebugSettings::EnumerateBackgroundTasks
 - shobjidl_core/IPackageDebugSettings::EnumerateBackgroundTasks
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
 - IPackageDebugSettings.EnumerateBackgroundTasks
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

An array of background task identifiers. You can use these identifiers in the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipackagedebugsettings-activatebackgroundtask">ActivateBackgroundTask</a> method to activate specified tasks.

### -param taskNames [out]

An array of task names that corresponds with background <i>taskIds</i>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Both parameters <i>taskIds</i> and <i>taskNames</i> have the same ordering of tasks. If you need to know the user-readable task name associated with <i>taskId[0]</i>, refer to <i>taskNames[0]</i>.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipackagedebugsettings">IPackageDebugSettings</a>