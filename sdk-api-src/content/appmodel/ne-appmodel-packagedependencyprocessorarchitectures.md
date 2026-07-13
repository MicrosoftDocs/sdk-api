---
UID: NE:appmodel.PackageDependencyProcessorArchitectures
tech.root: appxpkg
title: PackageDependencyProcessorArchitectures
ms.date: 7/12/2021
targetos: Windows
description: Defines the processor architectures for a framework package dependency that you create by using the TryCreatePackageDependency function.
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
 - PackageDependencyProcessorArchitectures
f1_keywords:
 - PackageDependencyProcessorArchitectures
 - appmodel/PackageDependencyProcessorArchitectures
dev_langs:
 - c++
---

## -description

Defines the processor architectures for a framework package dependency that you create by using the [TryCreatePackageDependency](nf-appmodel-trycreatepackagedependency.md) function.

## -enum-fields

### -field PackageDependencyProcessorArchitectures_None

No processor architecture is specified.

### -field PackageDependencyProcessorArchitectures_Neutral

Specifies the neutral architecture.

### -field PackageDependencyProcessorArchitectures_X86
 
Specifies the x86 architecture.

### -field PackageDependencyProcessorArchitectures_X64

Specifies the x64 architecture.

### -field PackageDependencyProcessorArchitectures_Arm

Specifies the ARM architecture.

### -field PackageDependencyProcessorArchitectures_Arm64

Specifies the ARM64 architecture.

### -field PackageDependencyProcessorArchitectures_X86A64

Specifies the x86/A64 architecture.

## -remarks

## -see-also

[TryCreatePackageDependency](nf-appmodel-trycreatepackagedependency.md)