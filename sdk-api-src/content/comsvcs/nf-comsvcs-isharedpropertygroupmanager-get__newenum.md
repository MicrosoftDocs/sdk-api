---
UID: NF:comsvcs.ISharedPropertyGroupManager.get__NewEnum
title: ISharedPropertyGroupManager::get__NewEnum (comsvcs.h)
description: Retrieves an enumerator for the named security call context properties.
helpviewer_keywords: ["ISharedPropertyGroupManager interface [COM+]","get__NewEnum method","ISharedPropertyGroupManager.get__NewEnum","ISharedPropertyGroupManager::get__NewEnum","_cos_ISharedPropertyGroupManager_get__NewEnum","comsvcs/ISharedPropertyGroupManager::get__NewEnum","cos.isharedpropertygroupmanager_get__newenum","get__NewEnum","get__NewEnum method [COM+]","get__NewEnum method [COM+]","ISharedPropertyGroupManager interface"]
old-location: cos\isharedpropertygroupmanager_get__newenum.htm
tech.root: cos
ms.assetid: 04e591c0-6bf4-4864-aaae-57ffd97c5414
ms.date: 12/05/2018
ms.keywords: ISharedPropertyGroupManager interface [COM+],get__NewEnum method, ISharedPropertyGroupManager.get__NewEnum, ISharedPropertyGroupManager::get__NewEnum, _cos_ISharedPropertyGroupManager_get__NewEnum, comsvcs/ISharedPropertyGroupManager::get__NewEnum, cos.isharedpropertygroupmanager_get__newenum, get__NewEnum, get__NewEnum method [COM+], get__NewEnum method [COM+],ISharedPropertyGroupManager interface
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - ISharedPropertyGroupManager::get__NewEnum
 - comsvcs/ISharedPropertyGroupManager::get__NewEnum
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ISharedPropertyGroupManager.get__NewEnum
---

# ISharedPropertyGroupManager::get__NewEnum


## -description

Retrieves an enumerator for the named security call context properties.

This property is restricted in Microsoft Visual Basic and cannot be used.

## -parameters

### -param retval [out]

A reference to the returned <a href="/windows/win32/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a> interface.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-isharedpropertygroupmanager">ISharedPropertyGroupManager</a>