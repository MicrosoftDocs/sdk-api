---
UID: NF:shobjidl_core.ISuspensionDependencyManager.RegisterAsChild
title: ISuspensionDependencyManager::RegisterAsChild (shobjidl_core.h)
description: ISuspensionDependencyManager::RegisterAsChild method
helpviewer_keywords: ["ISuspensionDependencyManager interface [Windows Shell]","RegisterAsChild method","ISuspensionDependencyManager.RegisterAsChild","ISuspensionDependencyManager::RegisterAsChild","RegisterAsChild","RegisterAsChild method [Windows Shell]","RegisterAsChild method [Windows Shell]","ISuspensionDependencyManager interface","shell.ISuspensionDependencyManager_RegisterAsChild","shobjidl_core/ISuspensionDependencyManager::RegisterAsChild"]
old-location: shell\ISuspensionDependencyManager_RegisterAsChild.htm
tech.root: shell
ms.assetid: DB9DDDA7-34AA-43D7-813B-C9A065383682
ms.date: 12/05/2018
ms.keywords: ISuspensionDependencyManager interface [Windows Shell],RegisterAsChild method, ISuspensionDependencyManager.RegisterAsChild, ISuspensionDependencyManager::RegisterAsChild, RegisterAsChild, RegisterAsChild method [Windows Shell], RegisterAsChild method [Windows Shell],ISuspensionDependencyManager interface, shell.ISuspensionDependencyManager_RegisterAsChild, shobjidl_core/ISuspensionDependencyManager::RegisterAsChild
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
 - ISuspensionDependencyManager::RegisterAsChild
 - shobjidl_core/ISuspensionDependencyManager::RegisterAsChild
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
 - ISuspensionDependencyManager.RegisterAsChild
---

# ISuspensionDependencyManager::RegisterAsChild


## -description

Registers the specified process as a child. This method is no longer supported on Windows 10, version 1809, and later versions.

## -parameters

### -param processHandle [in]

Type: <b>HANDLE</b>

The process to be registered as a child.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-isuspensiondependencymanager">ISuspensionDependencyManager</a>