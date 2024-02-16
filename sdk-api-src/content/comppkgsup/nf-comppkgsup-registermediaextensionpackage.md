---
UID: NF:comppkgsup.RegisterMediaExtensionPackage
tech.root: winprog
title: RegisterMediaExtensionPackage
ms.date: 02/15/2024
targetos: Windows
description: Registers the media extension with the given Package Family Name (PFN) for the current user.
prerelease: true
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Comppkgsup.dll
req.header: comppkgsup.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: Comppkgsup.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 11, version 24H2
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - comppkgsup.h
api_name:
 - RegisterMediaExtensionPackage
f1_keywords:
 - RegisterMediaExtensionPackage
 - comppkgsup/RegisterMediaExtensionPackage
dev_langs:
 - c++
helpviewer_keywords:
 - RegisterMediaExtensionPackage
---

## -description

Registers the media extension with the given Package Family Name (PFN) for the current user.


## -parameters

### -param packageFamilyName [in]

The Package Family Name of the media extension to be registered. For more information, see [An overview of Package Identity in Windows apps](/windows/apps/desktop/modernize/package-identity-overview).

## -returns

An HRESULT including the following values:

| Value | Description |
|-------|-------------|
| S_OK  | Success      |
| E_ACCESSDENIED | The API was called from a process that is not full-trust. |
| ERROR_INSTALL_FAILED | The specified Package Family Name was not found on the system. |

## -remarks

This API can be used to register media extensions that are already present in Windows but which have not yet been registered for the current user. Packages will not be automatically downloaded from the Microsoft Store. The API must be called from a full-trust process. For more information on the **Full Trust Permission Level** restricted capability. See [Restricted capability list](/windows/uwp/packaging/app-capability-declarations#restricted-capability-list).


## -see-also

