---
UID: NE:appmodel.AddPackageDependencyOptions
title: AddPackageDependencyOptions
description: Defines options that can be applied when adding a package dependency.
ms.date: 7/12/2021
tech.root: appxpkg
targetos: Windows
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
 - AddPackageDependencyOptions
f1_keywords:
 - AddPackageDependencyOptions
 - appmodel/AddPackageDependencyOptions
dev_langs:
 - c++
---

## -description

Defines options that can be applied when adding a run-time reference to a framework package by using the [AddPackageDependency](nf-appmodel-addpackagedependency.md) function.

## -enum-fields

### -field AddPackageDependencyOptions_None

No options are applied.

### -field AddPackageDependencyOptions_PrependIfRankCollision

If multiple packages are present in the package graph with the same rank as the call to [AddPackageDependency](./nf-appmodel-addpackagedependency.md), then the resolved package is added before others of the same rank. For more info, see **AddPackageDependency**.

## -remarks

## -see-also

[AddPackageDependency](./nf-appmodel-addpackagedependency.md)
