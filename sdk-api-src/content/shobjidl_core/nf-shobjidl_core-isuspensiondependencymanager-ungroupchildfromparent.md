---
UID: NF:shobjidl_core.ISuspensionDependencyManager.UngroupChildFromParent
title: ISuspensionDependencyManager::UngroupChildFromParent (shobjidl_core.h)
description: ISuspensionDependencyManager::UngroupChildFromParent method
helpviewer_keywords: ["ISuspensionDependencyManager interface [Windows Shell]","UngroupChildFromParent method","ISuspensionDependencyManager.UngroupChildFromParent","ISuspensionDependencyManager::UngroupChildFromParent","UngroupChildFromParent","UngroupChildFromParent method [Windows Shell]","UngroupChildFromParent method [Windows Shell]","ISuspensionDependencyManager interface","shell.ISuspensionDependencyManager_UngroupChildFromParent","shobjidl_core/ISuspensionDependencyManager::UngroupChildFromParent"]
old-location: shell\ISuspensionDependencyManager_UngroupChildFromParent.htm
tech.root: shell
ms.assetid: 4635FCD2-C49F-45F1-8D48-6BA418EBDFD0
ms.date: 12/05/2018
ms.keywords: ISuspensionDependencyManager interface [Windows Shell],UngroupChildFromParent method, ISuspensionDependencyManager.UngroupChildFromParent, ISuspensionDependencyManager::UngroupChildFromParent, UngroupChildFromParent, UngroupChildFromParent method [Windows Shell], UngroupChildFromParent method [Windows Shell],ISuspensionDependencyManager interface, shell.ISuspensionDependencyManager_UngroupChildFromParent, shobjidl_core/ISuspensionDependencyManager::UngroupChildFromParent
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
 - ISuspensionDependencyManager::UngroupChildFromParent
 - shobjidl_core/ISuspensionDependencyManager::UngroupChildFromParent
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
 - ISuspensionDependencyManager.UngroupChildFromParent
---

# ISuspensionDependencyManager::UngroupChildFromParent


## -description

Ungroups the specified child process from the parent process. This method is no longer supported on Windows 10, version 1809, and later versions.

## -parameters

### -param childProcessHandle [in]

Type: <b>HANDLE</b>

The child process to ungroup from the parent.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-isuspensiondependencymanager">ISuspensionDependencyManager</a>