---
UID: NE:appmodel.PackageDependencyLifetimeKind
tech.root: appxpkg
title: PackageDependencyLifetimeKind
ms.date: 7/12/2021
targetos: Windows
description: Specifies values that indicate the type of artifact that is used to define the lifetime of a package dependency.
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
 - PackageDependencyLifetimeKind
f1_keywords:
 - PackageDependencyLifetimeKind
 - appmodel/PackageDependencyLifetimeKind
dev_langs:
 - c++
---

## -description

Specifies values that indicate the type of artifact that is used to define the lifetime of a package dependency.

## -enum-fields

### -field PackageDependencyLifetimeKind_Process

The current process is the lifetime artifact. The package dependency is implicitly deleted when the process terminates.

### -field PackageDependencyLifetimeKind_FilePath

The lifetime artifact is an absolute filename or path. The package dependency is implicitly deleted when this is deleted.

### -field PackageDependencyLifetimeKind_RegistryKey

The lifetime artifact is a registry key in the format *root*\\*subkey*, where *root* is one of the following: HKEY_LOCAL_MACHINE, HKEY_CURRENT_USER, HKEY_CLASSES_ROOT, or HKEY_USERS. The package dependency is implicitly deleted when this is deleted.

## -remarks

## -see-also

[TryCreatePackageDependency](nf-appmodel-trycreatepackagedependency.md)
