---
UID: NF:shobjidl_core.ISuspensionDependencyManager.GroupChildWithParent
title: ISuspensionDependencyManager::GroupChildWithParent (shobjidl_core.h)
description: ISuspensionDependencyManager::GroupChildWithParent method
helpviewer_keywords: ["GroupChildWithParent","GroupChildWithParent method [Windows Shell]","GroupChildWithParent method [Windows Shell]","ISuspensionDependencyManager interface","ISuspensionDependencyManager interface [Windows Shell]","GroupChildWithParent method","ISuspensionDependencyManager.GroupChildWithParent","ISuspensionDependencyManager::GroupChildWithParent","shell.ISuspensionDependencyManager_GroupChildWithParent","shobjidl_core/ISuspensionDependencyManager::GroupChildWithParent"]
old-location: shell\ISuspensionDependencyManager_GroupChildWithParent.htm
tech.root: shell
ms.assetid: E9E5FDCB-83AA-4EC1-9CE2-1EABDD7DF39C
ms.date: 12/05/2018
ms.keywords: GroupChildWithParent, GroupChildWithParent method [Windows Shell], GroupChildWithParent method [Windows Shell],ISuspensionDependencyManager interface, ISuspensionDependencyManager interface [Windows Shell],GroupChildWithParent method, ISuspensionDependencyManager.GroupChildWithParent, ISuspensionDependencyManager::GroupChildWithParent, shell.ISuspensionDependencyManager_GroupChildWithParent, shobjidl_core/ISuspensionDependencyManager::GroupChildWithParent
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
 - ISuspensionDependencyManager::GroupChildWithParent
 - shobjidl_core/ISuspensionDependencyManager::GroupChildWithParent
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
 - ISuspensionDependencyManager.GroupChildWithParent
---

# ISuspensionDependencyManager::GroupChildWithParent


## -description

Groups the specified child process with the parent process. This method is no longer supported on Windows 10, version 1809, and later versions.

## -parameters

### -param childProcessHandle [in]

Type: <b>HANDLE</b>

The child process to group with the parent process.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-isuspensiondependencymanager">ISuspensionDependencyManager</a>