---
UID: NE:appmodel.AddPackageDependencyOptions2
title: AddPackageDependencyOptions2
description: Defines options (version 2) that can be applied when adding a package dependency.
ms.date: 02/05/2025
tech.root: appxpkg
targetos: Windows
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: appmodel.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 11, version 23H2 (10.0; Build 22631)
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
 - AddPackageDependencyOptions2
f1_keywords:
 - AddPackageDependencyOptions2
 - appmodel/AddPackageDependencyOptions2
dev_langs:
 - c++
---

## -description

Defines options (version 2) that can be applied when adding a run-time reference to a framework package by using the [AddPackageDependency2](./nf-appmodel-addpackagedependency2.md) function.

## -enum-fields

### -field AddPackageDependencyOptions2_None

No options are applied.

### -field AddPackageDependencyOptions2_PrependIfRankCollision

If multiple packages are present in the package graph with the same rank as the call to [AddPackageDependency2](./nf-appmodel-addpackagedependency2.md), then the resolved package is added before others of the same rank. For more info, see **AddPackageDependency2**.

### -field AddPackageDependencyOptions2_SpecifiedPackageFamilyOnly

Adds only the target package's family to the package graph. This provides you a way to more surgically manage your dependencies at runtime.

A Framework package can't declare dependencies in the Framework's manifest (that is, Framework package's dependency list is always a size of 1&mdash;`[TheFrameworkPackage]`. **AddPackageDependency2** targeting a Framework package adds only the target to the caller's package graph; a Framework package has declared dependencies. Thus targeting Framework packages avoids the need to restrict dynamic dependencies to the target's package family, but Framework packages can't replace Main packages for dynamic use because there are some things that only a Main package can do (for example, Packaged COM OOP Servers, windows.startupTask, and more). Main packages bring this additional indirect packages issue, and thus the need for the *AddPackageDependencyOptions2_SpecifiedPackageFamilyOnly* option, which narrows the scope of **AddPackageDependency2** to only the directly targeted package family.

## -remarks

## -see-also

* [AddPackageDependency2](nf-appmodel-addpackagedependency2.md)
