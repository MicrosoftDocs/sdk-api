---
UID: NE:appmodel.CreatePackageDependencyOptions
tech.root: appxpkg
title: CreatePackageDependencyOptions
ms.date: 7/12/2021
targetos: Windows
description: Defines options that can be applied when creating a package dependency by using the TryCreatePackageDependency function.
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: appmodel.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 11 (introduced in 10.0.22000.0)
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - appmodel.h
api_name:
 - CreatePackageDependencyOptions
f1_keywords:
 - CreatePackageDependencyOptions
 - appmodel/CreatePackageDependencyOptions
dev_langs:
 - c++
---

## -description

Defines options that can be applied when creating a package dependency by using the [TryCreatePackageDependency](nf-appmodel-trycreatepackagedependency.md) function.

## -enum-fields

### -field CreatePackageDependencyOptions_None

No options are applied.

### -field CreatePackageDependencyOptions_DoNotVerifyDependencyResolution

Disables dependency resolution when pinning a package dependency. This is useful for installers running as user contexts other than the target user (for example, installers running as LocalSystem).

### -field CreatePackageDependencyOptions_ScopeIsSystem

Defines the package dependency for the system, accessible to all users (by default, the package dependency is defined for a specific user). This option requires the caller has administrative privileges.

## -remarks

## -see-also

[TryCreatePackageDependency](nf-appmodel-trycreatepackagedependency.md)